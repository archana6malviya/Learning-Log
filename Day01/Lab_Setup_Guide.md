# Day01 - Lab setup guide

## 📌 Objective:
Install Oracle VirtualBox and set up virtual machines for Windows 10 and Ubuntu.

## 1. Install Oracle VirtualBox
### Steps:
1. Go to [https://www.virtualbox.org/](https://www.virtualbox.org/)
2. Download the version for your OS (Windows/macOS/Linux)
3. Run the installer and follow the default setup
4. Confirm installation by launching VirtualBox

## 2. Install Windows 10 VM
### Prerequisites:
- Windows 10 ISO from [Microsoft](https://www.microsoft.com/software-download/windows10ISO)

### Steps:
1. Open VirtualBox and click **New**
2. Name: `Windows10`
3. Type: Microsoft Windows | Version: Windows 10 (64-bit)
4. Assign RAM: At least 4GB
5. Create virtual hard disk: 50GB (VDI, dynamically allocated)
6. Start VM and select the Windows 10 ISO
7. Follow the Windows installation steps

### Clone Git Repository
1. Go to **git-scm.com** & download latest version.
2. Follow installation process.
3. Go to **cmd** on windows & Type **git clone https://github.com/archana6malviya/Learning-Log/edit/main**
4. All the file Will Download on your machine.


## 3. Install Ubuntu VM
### Prerequisites:
- Ubuntu ISO from [https://ubuntu.com/download](https://ubuntu.com/download)

### Steps:
1. Click **New** → Name: `Ubuntu22.04`
2. Type: Linux | Version: Ubuntu (64-bit)
3. Assign RAM: At least 2GB
4. Create virtual hard disk: 25GB (VDI, dynamically allocated)
5. Start VM and select the Ubuntu ISO
6. Follow the installation wizard

### Configure Ubantu Machine
1. Open Terminal
2. Type **sudo apt update** & type Password.- For update
3. Also **sudo apt install bzip2 tar gcc make perl git** & **Y**.- Required couple of package before installing guest addition CD.
4. Also **sudo apt install linux-headers-generic**- It install generic kernel headers which again is for installing guest edtiotion image.
5. Also **sudo apt install linux-headers-$(uname -r)**.- For latest kernel version.
6. CD icon will appear on screen.
7. Go to CD Directory from terminal.
8. Type **ls**.
9. Run **sudo ./VBoxlinuxaddition.run** .
10. type **sudo reboot now**.
11. For git **sudo apt install git**.
12. For Full screen- Go to **View** tab and **Full-screen Mode**.
13. Go to **Devices** & **shared clipboard** then **bidirectional**.
14. For removing unwanted icons on desktop- right click on icons -**eject** or **unpin**.
15. Also installed some packgages and dependency for course- run **cd install.sh/** & **ls** & **chmod +x ./install.sh** & **./install.sh**.


## ✅ Tips:
- Enable virtualization in BIOS if VMs don't start
- Use Guest Additions for better VM performance (available from VirtualBox menu)
- if there is warning after runing sudo update command then type what given in warning with sudo. then try again **sudo apt update**.
- If ubantu not start or stuck, try to power off and ON after sometimes it will load after sometime.
