# Captured real-time outputs of practiced Linux commands

# Process commands

- ps aux : Shows all running processes.
<img width="877" height="232" alt="image" src="https://github.com/user-attachments/assets/cb7cf132-3897-4a1e-bf86-32a835f0b90c" />

- ps -aux | head -n 3 : List running processes(top 3 lines).
<img width="856" height="343" alt="image" src="https://github.com/user-attachments/assets/9184e94d-ac28-436e-96be-961e389fbb33" />

- pgrep bash : Find process ID of bash (bash is running in PID 1 and PID 13)
<img width="391" height="183" alt="image" src="https://github.com/user-attachments/assets/521a19a1-1022-4d7f-9e92-20c4bed7ba63" />


- top : Live view of CPU, memory, and running processes
<img width="969" height="392" alt="image" src="https://github.com/user-attachments/assets/aa80d4a0-cbf8-4923-a921-e2487579e53f" />


# Service commands

- systemctl status - Checks if a service is running or not
<img width="1899" height="774" alt="image" src="https://github.com/user-attachments/assets/990eaa31-d7de-49df-a17c-7c6bcd8906c0" />

- systemctl status sshd : It tells you whether the SSH server is running or not on your system.
<img width="1920" height="502" alt="image" src="https://github.com/user-attachments/assets/69b1e8b2-6489-4983-8354-23c5ca224ad4" />

- systemctl list-units --type=service : shows all active services running in Linux system
<img width="1494" height="710" alt="image" src="https://github.com/user-attachments/assets/77bce039-b79b-4b8c-9236-a972e9513233" />


# Log commands

- journalctl -u sshd : Shows logs for the SSH service (helpful for debugging service issues)
<img width="1920" height="706" alt="image" src="https://github.com/user-attachments/assets/dc770934-a9a7-4bec-bb3d-405434dd83f8" />

- tail -50 error.log-20260530 : Shows the last 50 lines of the file error.log-20260530.
<img width="1920" height="773" alt="image" src="https://github.com/user-attachments/assets/dfb2557e-e456-4421-bf40-3387dfc0dc1b" />


# Service for inspection (SSH)

- systemctl status docker
<img width="1920" height="614" alt="image" src="https://github.com/user-attachments/assets/364bcefe-5d82-4acb-8d34-4d052b460835" />

- systemctl show sshd : Displays detailed configuration and properties of the SSH service.
<img width="1920" height="728" alt="image" src="https://github.com/user-attachments/assets/3b97413c-6324-4e29-9981-4c90c3859ec0" />

- systemctl is-enabled sshd : Checks whether SSH starts automatically when the server boots.
<img width="1920" height="171" alt="image" src="https://github.com/user-attachments/assets/df7bb476-a545-49b7-b17f-643857d736b6" />



It is running now lets stop it. And try to connect to localhost.
- sudo systemctl stop sshd : Stop service
<img width="1920" height="151" alt="image" src="https://github.com/user-attachments/assets/5309333e-ca21-4968-b357-56041e78c2a9" />

- sudo systemctl status sshd : Verify the service is stopped
- Observation: SSH service is inactive (dead).


Error :
- ssh localhost : Try connecting to localhost
- output - ssh: connect to host localhost port 22: Connection refused
- Observation: Connection failed because the SSH service is not running.
<img width="1920" height="118" alt="image" src="https://github.com/user-attachments/assets/5d34fefa-3173-4900-94c1-3438fd5bb349" />


Let's view logs and check
- sudo journalctl -u sshd --no-pager | tail : Check SSH service logs
- Observation: Logs show that the SSH service was stopped successfully.
<img width="1920" height="359" alt="image" src="https://github.com/user-attachments/assets/3c5361bc-479c-41ab-a18d-59fd708fc786" />


Log shows the service is stopped let's start the ssh service and check again
- sudo systemctl start sshd : Start the SSH service again
- ps -aux | grep sshd : SSH daemon process is running.
<img width="1920" height="193" alt="image" src="https://github.com/user-attachments/assets/75f6c90c-3456-4582-ae6f-cec9406e79f2" />

- sudo systemctl status sshd : Verify the service is running
<img width="1920" height="457" alt="image" src="https://github.com/user-attachments/assets/acc88656-54b5-40ca-b7b8-277aeec7238c" />

- ssh localhost : Try connecting again
- Observation:
The connection reaches the SSH server.
If authentication is configured correctly, login succeeds.
<img width="1920" height="529" alt="image" src="https://github.com/user-attachments/assets/ae038ae6-eb35-43ca-900f-964711f6d151" />



