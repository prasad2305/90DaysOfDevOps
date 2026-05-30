# Core Components of Linux
- Hardware:
The physical parts of a computer like processor, memory, and disk where Linux runs.
- Kernel:
The main core of Linux. It controls everything like memory, CPU, and devices, and connects software with hardware.
- Shell:
A way to give commands to Linux. It takes your commands and passes them to the kernel.
- GUI (Graphical User Interface):
Graphical user interface for visual interaction.
- System Libraries:
Pre-written functions that help applications use system features without doing everything from scratch.
- System Utilities:
Basic built-in tools and commands like ls, cp, mv, used to manage files and system tasks.

# Processes in Linux
When you run any command or program in Linux, it becomes a process.

- When you open a terminal, it runs as a process.
- When you play music, the music player becomes a process.

# Process States (Simple Explanation)
- Running:
The process is actively working.
- Sleeping:
The process is waiting or idle (not doing anything at the moment).
- Stopped:
The process is paused (for example using Ctrl+Z or Ctrl+C) and can be started again.
- Zombie:
The process has finished, but its information is still in the system because the parent process has not yet cleaned it up.

# 5 Commands used daily
- ps / top:
Shows running processes with details like CPU usage, memory usage, and process ID. Used for monitoring system performance.
- chmod:
Used to change file permissions (read, write, execute).
- ssh:
Used to securely connect to a remote server from another machine.
- systemctl:
Used to manage system services like starting, stopping, or checking status.
- df / du:
df shows overall disk space usage of the system.
du shows the size of a specific file or folder.
