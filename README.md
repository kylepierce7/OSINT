# OSINT
OSINT VM Ubuntu 22.04 LTS 

Ideas sourced from Michael Bazzell: OSINT TECHNIQUES 

https://inteltechniques.com/

## BUILD NOTES

- HYBERVISOR: Oracle VM VirtualBox
- Created a Default Ubuntu 22.04LTB VM: UBUNTU ORIGINAL
- Install VirtualBox Guest Additions:
``` 
sudo apt update
sudo apt install build-essential dkms linux-headers-$(uname -r)
```
Click on Devices / Insert Guest Additions CD Image
```
sudo mkdir -p /mnt/cdrom
sudo mount /dev/cdrom /mnt/cdrom
cd /mnt/cdrom
sudo ./VBoxLinuxAdditions.run
```

- Check boot | Clone build and name: OSINT Original
- edit password file
``` 
sudo nano /etc/pam.d/common-password
```
- find line with "password success= .....pam_unix. ...." 
- append `minlen=<desiredNumber>`
- save file
NOTE: did not work....


