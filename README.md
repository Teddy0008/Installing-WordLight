

# WordLight Installation Guide
This is a guide on how to install WordLight on almost any Operating System

## Windows
1. Download the installer from the [official WordLight website](https://revivalnsw.com.au/resources/wordlight/)
2. Open the executable file you just downloaded
   1. If a "Windows protected your PC" prompt appears, click on "More info" and then click "Run anyway"
   2. If a User Account Control prompt appears, click Yes
3. When the installer opens up, click the "Install" button and wait for WordLight to install
4. When it is done installing, click "Finish"

## MacOS
1. Download [Parallels Desktop](https://www.parallels.com/products/desktop/) from the official site
2. Follow the instructions in the installer to install Windows 11 on Parallels Desktop
3. Once you're in Windows 11, follow the installation guide for Windows above

## Linux
Since there are so many Linux Distributions, I only cover the base ones.
### Ubuntu & Debian
1. Install Wine
	1. Refresh the repositories with this command:
	```bash
	sudo apt update
	```
	2. Install Wine with this command:
	```bash
	sudo apt install wine64
	```
2. Install the Segoe UI font
	1. Install git if you don't have it
	```bash
	sudo apt install git
	```
	2. Clone a Segoe UI font repository
	```bash
	git clone https://github.com/mrbvrz/segoe-ui-linux
	``` 
	3. Get into the directory of the newly cloned repository
	```bash
	cd segoe-ui-linux
	```
	4. Change the permissions to be able to execute the install script
	```bash
	chmod +x install.sh
	```
	5. Run the install script
	```bash
	sudo ./install.sh
	```
3. Download and install WordLight
	1. Download the installer from the [official WordLight website](https://revivalnsw.com.au/resources/wordlight/)
	2. Open a terminal in the directory where you downloaded the installer and run this command:
	```bash
	wine64 WordLightSetup.exe
	```
	3. Follow the instructions 3-4 in the Windows installation guide
### Fedora
1. Install Wine
	1. Refresh the repositories with this command:
	```bash
	sudo dnf upgrade --refresh
	```
	2. Install Wine with this command:
	```bash
	sudo dnf install wine
	```
3. Install the Segoe UI font
	1. Install yay
		1. Download the font file from [here](https://raw.githubusercontent.com/Teddy0008/Installing-WordLight/main/segoeui.ttf)
		2. Make a TrueType Font folder
		```bash
		mkdir /usr/share/fonts/ttf
		```
		3. Open a terminal in the directory where you downloaded the font and copy the font to the ttf directory with this command:
		```bash
		cp segoeui.ttf /usr/share/fonts/ttf
		```
		4. Update the font cache
		```bash
		fc-cache -v
		```
4. Download and install WordLight
	1. Download the installer from the [official WordLight website](https://revivalnsw.com.au/resources/wordlight/)
	2. Open a terminal in the directory where you downloaded the installer and run this command:
	```bash
	wine64 WordLightSetup.exe
	```
	3. Follow the instructions 3-4 in the Windows installation guide
### openSUSE
1. Install Wine
	1. Add the wine repository:
		1. Download the repository key
		```bash
		wget https://download.opensuse.org/repositories/Emulators:/Wine/openSUSE_Tumbleweed/repodata/repomd.xml.key 
		```
		2. Install the key
		```bash
		sudo rpm --import repomd.xml.key
		```
		3. Add the repository
		```bash
		sudo zypper addrepo https://download.opensuse.org/repositories/Emulators:/Wine/openSUSE_Tumbleweed/Emulators:Wine.repo
		```
		4. Update the package database
		```bash
		sudo zypper refresh
		```
	2. Install Wine with this command:
	```bash
	sudo zypper install wine
	```
3. Install the Segoe UI font
	1. Install yay
		1. Download the font file from [here](https://raw.githubusercontent.com/Teddy0008/Installing-WordLight/main/segoeui.ttf)
		2. Make a TrueType Font folder
		```bash
		mkdir /usr/share/fonts/ttf
		```
		3. Open a terminal in the directory where you downloaded the font and copy the font to the ttf directory with this command:
		```bash
		cp segoeui.ttf /usr/share/fonts/ttf
		```
		4. Update the font cache
		```bash
		fc-cache -v
		```
4. Download and install WordLight
	1. Download the installer from the [official WordLight website](https://revivalnsw.com.au/resources/wordlight/)
	2. Open a terminal in the directory where you downloaded the installer and run this command:
	```bash
	wine64 WordLightSetup.exe
	```
	3. Follow the instructions 3-4 in the Windows installation guide
### Arch Linux
1. Install Wine
	1. Enable the multilib repository
		1. Install nano
		```bash
		sudo pacman -S nano
		```
		2. Open the pacman config file
		```bash
		sudo nano /etc/pacman.conf
		```
		3. Find where it says:
		```
		# [multilib]
		# Include /etc/pacman.d/mirrorlist
		```
		4. Uncomment those lines by removing the **#** symbols, should look like this:
		```
		[multilib]
		Include = /etc/pacman.d/mirrorlist
		```
	2. Refresh the repositories with this command:
	```bash
	sudo pacman -Sy
	```
	3. Install Wine with this command:
	```bash
	sudo pacman -S wine
	```
3. Install the Segoe UI font
	1. Install yay
		1. Install the basic tools and git
		```bash
		sudo pacman -S --needed base-devel git
		```
		2. Clone the yay repository
		```bash
		git clone https://aur.archlinux.org/yay.git
		```
		3. Get into the directory of the newly cloned repository
		```bash
		cd yay
		```
		4. Build the package
		```bash
		makepkg -si
		```
	2. Use yay to install the default Windows 11 fonts (including Segoe UI)
	```bash
	yay -S ttf-ms-win11-auto --noconfirm
	```
4. Download and install WordLight
	1. Download the installer from the [official WordLight website](https://revivalnsw.com.au/resources/wordlight/)
	2. Open a terminal in the directory where you downloaded the installer and run this command:
	```bash
	wine64 WordLightSetup.exe
	```
	3. Follow the instructions 3-4 in the Windows installation guide
