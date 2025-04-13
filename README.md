# Docker-Installation
docker installation
## Step 1: Make sure to provision three virtual machines using oracle virtual box
- Ensure to provision one virtual machine to install & configure jenkins and ansible(master node)
- Ensure to provison two virtual machines (Slave node)
- Make sure to generate SSH key in master node
   **- ssh-keygen -t rsa -b 4096 -C "jenkins@ansible"**__
- Make sure to copy the generated ssh key to slave nodes
  **- ssh-copy-id ubuntu@192.168.1.10
    - ssh-copy-id ubuntu@192.168.1.11**
- Make sure to update the etc file to ensure paswword less authentication and restart ssh server
  **-sudo nano /etc/ssh/sshd_config
   -PasswordAuthentication yes
   -PermitRootLogin no**
  **sudo systemctl restart ssh**
- Make sure to update priveliages access in all the threee nodes
  **ubuntu ALL=(ALL:ALL) NOPASSWD: ALL**
  **guest ALL=(ALL:ALL) NOPASSWD: ALL**
  **kafka ALL=(ALL:ALL) NOPASSWD: ALL**
  



