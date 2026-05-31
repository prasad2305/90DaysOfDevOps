# Linux User & Group Management

## Users Created

- Create user : ` useradd -m <username>`

- Check user info : `cat /etc/passwd | grep <username>`

<img width="1920" height="413" alt="image" src="https://github.com/user-attachments/assets/7cd0a17c-c031-4773-9b2f-457b75a38396" />

<img width="1920" height="254" alt="image" src="https://github.com/user-attachments/assets/f355758e-6f23-4db5-aa73-8d0b52df28cb" />


- Users: tokyo, berlin, professor

## Groups Created

- Create group : `groupadd <groupname>`

- Check group : `cat /etc/group | grep <groupname>`

<img width="1920" height="288" alt="image" src="https://github.com/user-attachments/assets/bed68fb5-9b16-4182-85ee-9b37c2727279" />

- Groups: developers, admins

## Assign Users to Groups

- Add user to single group : `usermod -aG <groupname> <username>`

- Add user to multiple groups : `usermod -aG <group1>,<group2> <username>`

- Check user groups : `groups <username>`

<img width="1920" height="399" alt="image" src="https://github.com/user-attachments/assets/86f2524f-3187-4218-b693-728185bfc3a3" />


## Directories Created

- Create directory : `mkdir -p <directory_path>`

- Check directory : `ls -ld <directory_path>`

<img width="1920" height="392" alt="image" src="https://github.com/user-attachments/assets/b45082b8-dcab-456c-a7dd-be90bac1c5ff" />



## Home directories of Users

<img width="1920" height="198" alt="image" src="https://github.com/user-attachments/assets/04280202-3fdb-40ba-a141-4b5fdc3331e3" />


## Shared Directory

- Change group ownership : `chgrp <groupname> <directory_path>`

- Change owner : `chown <user>:<group> <directory_path>`

- Set permissions : `chmod <permission_number> <directory_path>`

<img width="1920" height="418" alt="image" src="https://github.com/user-attachments/assets/615dafef-53a1-4a18-8675-61679a273fc5" />

## Team Workspace

- Test command as user : `sudo -u <username> touch <file_path>`

<img width="1920" height="594" alt="image" src="https://github.com/user-attachments/assets/472e14a0-ee14-4167-bea7-92b3e7a64a37" />


## What I learned

* Learned to create and manage Linux users using useradd and passwd.
* Learned to create and manage groups using groupadd.
* Learned to assign users to groups using usermod -aG.
* Learned how users can belong to multiple groups for access control.
* Learned Linux file permissions using chmod (rwx system).
* Learned ownership management using chgrp command.
* Learned to create shared directories using mkdir -p.
* Learned to test user access using sudo -u command.
* Learned to verify users and groups using /etc/passwd and /etc/group.
* Learned basic Linux access control for team collaboration.

