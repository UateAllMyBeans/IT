Tegin 15 student kasutajat, iga kasutaja nimega student(number). Lisasin need kasutajad gruppi "students"

Commands: 
sudo adduser student2,
sudo groupadd students,
sudo usermod -aG students student1-16.

Tegin Samba shared folderisse uue directory "students" 

Commands: 
sudo mkdir -p /shared/students, 
sudo chown root:students /shared/students, 
sudo chmod 770 /shared/students. 

Tegin igale studentile enda folderi.

Commands: 
sudo mkdir /shared/students/student1-16, 
sudo chown student1-16:students /shared/students/student1-16, 
sudo chmod 700 /shared/students/student1-16,
sudo smbpasswd -a student1-16.

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
