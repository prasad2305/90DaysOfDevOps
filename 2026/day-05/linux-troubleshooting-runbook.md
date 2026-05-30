

# Environment basics
- Command : uname -a (Tells you what kernel and architecture the system is using.)
<img width="1920" height="235" alt="image" src="https://github.com/user-attachments/assets/ea161e73-39cc-403d-8602-3dc5e491a47f" />

- Command : cat /etc/os-release (Tells you which Linux distribution and version is installed.)
<img width="1920" height="450" alt="image" src="https://github.com/user-attachments/assets/e89a7763-2e20-4c96-9480-5d012d9b1dc8" />

# Filesystem sanity 
- mkdir /tmp/runbook-demo : Creates a temporary directory for testing file operations.
- cp /etc/hosts /tmp/runbook-demo/hosts-copy && ls -l /tmp/runbook-demo : Copy a file and verify
    
<img width="1920" height="387" alt="image" src="https://github.com/user-attachments/assets/0d0fa294-c3ed-4279-a001-0141d68e299d" />

# CPU / Memory
- top (Real-time process monitoring)
<img width="1920" height="705" alt="image" src="https://github.com/user-attachments/assets/ca3f64cf-43f0-41b6-b649-8e5bf942498b" />

- ps -o pid,pcpu,pmem,comm -p 1 (Monitor a specific process)
<img width="1920" height="302" alt="image" src="https://github.com/user-attachments/assets/b1702126-0dea-4853-b44d-a091ebdcb720" />

- free -h (Check memory usage)
<img width="1920" height="262" alt="image" src="https://github.com/user-attachments/assets/ce79305b-cf2a-4587-a5d3-cd37f858cf17" />


# Disk / IO
- df -h 
<img width="1920" height="344" alt="image" src="https://github.com/user-attachments/assets/a9d34225-b13a-4285-8dfb-9eb13cbffa19" />

- sudo du -sh /var/log
<img width="1920" height="224" alt="image" src="https://github.com/user-attachments/assets/cf13600c-39a5-4f94-9dba-237307726c7c" />


- iostat
<img width="1920" height="366" alt="image" src="https://github.com/user-attachments/assets/aac2ff09-6688-42b9-bcdd-1f1180e24259" />


# Network

- sudo ss -tulpn | grep  sshd
<img width="1920" height="246" alt="image" src="https://github.com/user-attachments/assets/e420ac62-c9fe-40d1-95b4-03c6f1789dbe" />

- netstat -tulpn
<img width="1920" height="438" alt="image" src="https://github.com/user-attachments/assets/8aeeaf9f-23f1-4cbe-8823-d6f37b3e669e" />






