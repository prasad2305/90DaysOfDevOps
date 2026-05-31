# File Permissions & File Operations Challenge

## Create Files

- Create empty file devops.txt using touch
- Create notes.txt with some content using cat or echo
- Create script.sh using vim with content: echo "Hello DevOps"
- Verify: ls -l to see permissions

<img width="1920" height="439" alt="image" src="https://github.com/user-attachments/assets/f6fc0d50-de48-40c7-bc92-f6d29c64301a" />

## Read Files

- Read notes.txt using cat

<img width="1920" height="223" alt="image" src="https://github.com/user-attachments/assets/85c432f8-a023-4f41-9a3b-746cfb82da6a" />

- View script.sh in vim read-only mode

<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/291efa23-b31b-44eb-a703-46877fe4f43f" />


- Display first 5 lines of /etc/passwd using head

<img width="1920" height="365" alt="image" src="https://github.com/user-attachments/assets/1d0d1208-58ef-4fb4-b06e-af2ee0e3ac05" />


- Display last 5 lines of /etc/passwd using tail

<img width="1920" height="317" alt="image" src="https://github.com/user-attachments/assets/42ebe1df-f58f-49f9-ae58-03a5fed8fa73" />


## Understand Permissions

- Understand Permissions

  All three files (devops.txt, notes.txt, script.sh) have: rw-r--r--

  - Owner (ec2-user) → can read and write
  - Group (ec2-user group) → can only read
  - Others (everyone) → can only read

<img width="1920" height="193" alt="image" src="https://github.com/user-attachments/assets/5bbe8b81-cf12-47ef-9c5a-25683822b2be" />


## Modify Permissions

- Make script.sh executable → run it with ./script.sh

<img width="1920" height="125" alt="image" src="https://github.com/user-attachments/assets/536b20b2-10ae-4d0d-a0b4-844d00b6210a" />


- Set devops.txt to read-only (remove write for all)

<img width="1920" height="520" alt="image" src="https://github.com/user-attachments/assets/9170f8d6-7650-481d-abdb-f639d442776c" />

  
- Set notes.txt to 640 (owner: rw, group: r, others: none)

<img width="1920" height="629" alt="image" src="https://github.com/user-attachments/assets/5181a37c-2820-4a16-a13e-ba3e71b8a847" />

  
- Create directory project/ with permissions 755

<img width="1920" height="299" alt="image" src="https://github.com/user-attachments/assets/804f6c98-b14c-4c1b-bc4e-50b8199eb431" />


## Test Permissions

- Try writing to a read-only file
  
- File is read-only, so write operation is not allowed.

<img width="1920" height="417" alt="image" src="https://github.com/user-attachments/assets/77b6a421-9474-4b4b-8766-501f52c5b43d" />

- Try executing a file without execute permission

- File does not have execute (x) permission, so Linux blocks execution.

<img width="1920" height="425" alt="image" src="https://github.com/user-attachments/assets/a9d63721-ea2d-484c-9077-3674576368ad" />



## Linux Commands Use 

t* ouch devops.txt → Create empty file
* echo "text" > notes.txt → Create file with content
* echo 'echo "Hello DevOps"' > script.sh → Create script file
* vim script.sh → Edit file in vim
* ls -l → Check file permissions
* cat notes.txt → Read full file content
* vim -R script.sh → Open file in read-only mode
* head -5 /etc/passwd → Show first 5 lines
* tail -5 /etc/passwd → Show last 5 lines
* chmod +x script.sh → Make script executable
* ./script.sh → Run script
* chmod 444 devops.txt → Make file read-only
* chmod 640 notes.txt → Set owner rw, group r, others none
* mkdir project → Create directory
* chmod 755 project → Set directory permissions
* echo "test" >> devops.txt → Try writing to file
* ./script.sh → Try executing script

## What I Learned

* Learned Linux file operations like create, read, and edit files using touch, echo, cat, and vim.
* Understood Linux permissions system (rwx) and how to manage access using chmod.
* Learned to execute scripts and handle permission errors in Linux.
