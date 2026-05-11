Tegin 15 student kasutajat, iga kasutaja nimega student(number). Command: sudo adduser student2
Siis lisasin need kasutajad gruppi "students" Command: sudo groupadd students, sudo usermod -aG students student1-16.
Tegin Samba shared folderisse uue directory "students" Command: sudo mkdir -p /shared/students, lisasin omanikuõigused sudo chown root:students /shared/students, sudo chmod 770 /shared/students. Tegin igale studentile enda folderi. Command: sudo mkdir /shared/students/student1-16, sudo chown student1-16:students /shared/students/student1-16, sudo chmod 700 /shared/students/student1-16. sudo smbpasswd -a student1-16
Nüüd on nii, et student1 saab student1 folderile ligi, aga näiteks student2 folderile ei saa ligipääsu. 
Tegin kasutaja "teacher" mis saab pääseda igasse student folderisse. Command: sudo groupadd teachers, sudo adduser teacher, sudo usermod -aG teachers teacher, sudo chgrp teachers /shared/students/student1-16, sudo chmod 770 /shared/students/student1-16.
