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

## ✅ Tips:
- Enable virtualization in BIOS if VMs don't start
- Use Guest Additions for better VM performance (available from VirtualBox menu)
