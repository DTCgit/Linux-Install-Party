# Linux Install Party :penguin:

This guide will help you to install Ubuntu 22.10 (Kinetic Kudu) Daily Build on a virtual machine.

Made with :heart: by Youssef HABIBI ([@YHbibi](https://github.com/YHbibi)).

---

## Prerequisites

- 2 GHz dual-core processor or better
- 8 GB RAM or more
- 25 GB of available disk space minimum

## Steps

1. [Download an Ubuntu Image](#1-Download-an-Ubuntu-Image)
2. [Download and install VirtualBox](#2-Download-and-Install-Virtualbox)
3. [Create a new virtual machine](#3-Create-a-new-virtual-machine)
4. [Install your image](#4-Install-your-image)
5. [Installing Guest Additions](#5-installing-Guest-Additions)

## 1. Download an Ubuntu Image

You can download an Ubuntu image [here](https://ubuntu.com/download/desktop). Make sure to save it to a memorable location on your PC.
We will use the Ubuntu 22.10

![ubuntu download](images/ubuntu-download.png)

> Download may take a while as the file size for Ubuntu 22.10 is 3.8 GB

## 2. Download and install VirtualBox

### 1. Download VirtualBox

Download the latest version of VirtualBox from [here](https://www.virtualbox.org/wiki/Downloads).

![virtualbox download](images/virtualbox-download.png)

### 2. install VirtualBox

Once you have completed the installation, run the `.exe` file and install VirtualBox.

## 3. Create a new virtual machine

1. Start VirtualBox, and click on the top menu: `Machine->New` (or press CTRL-N).

   ![create new](images/create-new.png)

2. Provide name, for example, Ubuntu 22.10. The type would be set to Linux automatically.

   ![vm name](images/vm-name.png)

3. Set Memory Size = 2048 MB(2GB)

   ![memory-size](images/memory-size.png)

4. Select ‘Create a virtual hard disk now’, click `Create` button.

   ![hard disk](images/hard-disk.png)

5. Select the radio button to use VDI format for the virtual disk.

   ![hard disk type file](images/hard-disk-type-file.png)

6. Choose “Dynamically allocated”.

   ![storage on physical disk](images/storage-on-physical-disk.png)

7. Allocate at Minimum 25 GB

   ![size vm](images/size-vm.png)

8. After this click Create to initialize the machine!

9. Next, click to highlight your new VM in the left-hand menu and select `Settings->System->Processor`.

   ![cpu setting](images/cpu.png)

10. Navigate to `Storage` on the left-hand menu and select the `Storage` tab. Click on the icon of the CD-ROM drive (which is now empty). On the right, under `Optical Drive`, click on the CD icon with the down arrow and select `Choose a disk file...` Navigate to the earlier downloaded Ubuntu ISO.

    ![Choose the disc image](images/choose-the-disc-image.png)

Click **OK** .

## 4. Install your image

1. Double click on the newly created virtual machine.

   ![boot the vm](images/boot-vm.png)

   > Ubuntu desktop should now boot and display the installation menu.

2. Choose the language and click `Install Ubuntu`.

   ![install ubuntu](images/install-ubuntu.png)

3. You will be asked to select your keyboard layout. Once you’ve chosen one, click `Continue`.

   ![choose the keyboard layout](images/select-keyboard-layout.png)

4. Next, you will be prompted to choose between the Normal installation and Minimal installation options. The minimal installation is useful for those with smaller hard drives or who don’t require as many pre-installed applications.In Other options, you will be prompted to download updates as well as third-party software that may improve device support and performance (for example, Nvidia graphics drivers) during the installation. It is recommended to check both of these boxes. If you are not currently connected to the internet, you will be prompted to do so at this point. Ensure you are able to remain connected throughout the installation.

   ![Installation Setup](images/download-updates.png)

5. This screen allows you to configure your installation. If you would like Ubuntu to be the only operating system on your device, select Erase disk and install Ubuntu.

   ![Installation type](images/installation-type.png)

6. Select your location and timezone from the map screen and click Continue. This information will be detected automatically if you are connected to the internet.

   ![Select location](images/select-location.png)

7. On this screen, you will be prompted to enter your name and the name of your computer as it will appear on the network. Finally, you will create a username and a strong password.

   ![login details](images/login-details.png)

8. Now sit back and enjoy the slideshow as Ubuntu installs in the background! :blush:

   ![complete installation](images/complete-installation.png)

9. Once the installation has completed, you will be prompted to restart your machine. Click **Restart Now**.

   ![restart vm](images/restart-now.png)

10. When you restart, enter your password on the login screen (assuming you selected that option when creating your login details).

## 5. Installing Guest Additions

Guest Additions is an extra piece of software that unlocks some more advanced features of VirtualBox. This includes better integration between your virtual machine and the host machine.

1. Open a terminal window and run

   ```
   sudo apt update
   sudo apt install build-essential dkms linux-headers-$(uname -r)
   ```

2. Click on `Devices > Insert Guest Additions CD image...`

   ![guest addition](images/guest_addition.png)

3. The disc will appear inside your virtual desktop and you will be prompted to run the software.

   ![window resolution](<images/pasted%20image%200%20(1).png>)

   Enter your password to install it.
   Once this is complete, you will need to restart your virtual machine for the new features to take effect.

# Conclusion

**Having Fun With the Linux Command Line**

The Linux terminal is an efficient tool. You can develop and write commands while carrying out daily tasks and use it to command the entire system.

And remember that Linus Torvalds said :

> In real open source, you have the right to control your own destiny. :wink:
