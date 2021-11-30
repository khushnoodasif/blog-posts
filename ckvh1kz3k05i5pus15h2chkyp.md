## How to Reset Password in Kali Linux 2021

Kali Linux is the most popular security operating system of today, and it is the operating system that most programmers use for penetration testing. Pen-testing is a practice in which people check their own systems and their own architectures for vulnerabilities. Debian-based, it is widely regarded as one of the best options for hackers. Kali Linux was developed by offensive security as a rewrite of Backtrack, a Linux distribution focused on security. Kali Linux is a distribution with many hacking and penetration tools that are current and are included as part of the distribution by default.

Kali Linux requires a minimum of 20GB of storage space and 1GB of RAM for its installation and operation. The operating system uses a number of tools that require graphics hardware acceleration.

**Reset Root Password**

If you have forgotten your Kali Linux system password all you need to do is follow the steps below. 

1. Restart the system
2. Enter the GRUB menu and cancel the timeout with any key on the keyboard. So, the system won't boot into Kali. 
3. Select the 'Advanced options for Kali GNU/Linux' option and press 'E' on the keyboard.
4. Go to the line with 'linux' on the command line. Replace 'o' with 'w' in the Linux line so that it becomes 'rw_single'. At the very end of this line, hit the space bar on your keyboard and type 'init=/bin/bash'.
5. Save the changes by pressing Fn + F10.
6. Enter 'passwd' into the command emulator and press Enter. 
7. Enter your new password next to the 'New Password' option and press Enter. Once you have retyped your new password, you will see the message 'password updated successfully'.
8. You can now return to the login screen and log back into your Kali Linux System.