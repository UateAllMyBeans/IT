Tegin 15 student kasutajat, iga kasutaja nimega student(number). Lisasin need kasutajad gruppi "students"



Commands: 
sudo adduser student2,
sudo groupadd students,
sudo usermod -aG students student1-16.

---

Tegin Samba shared folderisse uue directory "students" 



Commands: 
sudo mkdir -p /shared/students, 
sudo chown root:students /shared/students, 
sudo chmod 770 /shared/students. 

---

Tegin igale studentile enda folderi.

Commands: 
sudo mkdir /shared/students/student1-16, 
sudo chown student1-16:students /shared/students/student1-16, 
sudo chmod 700 /shared/students/student1-16,
sudo smbpasswd -a student1-16.

---

Tegin kasutaja "teacher" mis saab pääseda igasse student folderisse. 

Commands: 
sudo groupadd teachers, 
sudo adduser teacher, 
sudo usermod -aG teachers teacher, 
sudo chgrp teachers /shared/students/student1-16, 
sudo chmod 770 /shared/students/student1-16.

Kokkuvõte:
Student1 saab student1 folderile ligi, aga näiteks student2 folderile ei saa ligipääsu. Teacher saab igat folderi accessida.
Iga studenti parool on student(number), näiteks kasutaja: student1 parool: student1 

---

Lisasime Dockeri, et serveri haldus ja kasutus oleks lihtsam ja saaks kasutada kindlaid programme vajadusel

Commands: sudo apt update
          sudo apt install ca-certificates curl gnupg -y

Lisasime Docker’i, et serveris oleks võimalik vajadusel teenuseid konteinerites käivitada.

Commands:
sudo apt update
sudo apt install ca-certificates curl gnupg -y
sudo install -m 0755 -d /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
sudo chmod a+r /etc/apt/keyrings/docker.gpg
sudo apt update
sudo apt install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin -y

---

Kontrollisin, et Docker töötab.

Commands:
sudo systemctl status docker
sudo docker --version
sudo docker compose version
sudo docker run hello-world

Kokkuvõte: Docker on serverisse paigaldatud ja töötab. Hello-world test kinnitas, et konteinerid käivituvad korrektselt.
