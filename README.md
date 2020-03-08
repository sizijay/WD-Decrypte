## WD-Decrypte
The Western Digital Decryption tools
this repo relates to this Tutorial : https://youtu.be/Qz51UelzByA

## The youtube notes : 
* [Notes for WD DECRYPTION]( https://github.com/SifoHamlaoui/Youtube_Notes/blob/master/HOW%20TO%20DECRYPTE%20Western%20Digital%20DRIVE%20ON%20LINUX.md)
## The Files : 
* [1002.pdf](https://github.com/SifoHamlaoui/WD-Decrypte/blob/master/1002.pdf) & [WD_Encryption_API.txt](https://github.com/SifoHamlaoui/WD-Decrypte/blob/master/WD_Encryption_API.txt) : shows the API & the Algorithms used for the encryption 
* [cookpw.py](https://github.com/SifoHamlaoui/WD-Decrypte/blob/master/cookpw.py) : generate's the .BIN file ( 40bytes ) containes the decryption password 

 * [drive.sh](https://github.com/SifoHamlaoui/WD-Decrypte/blob/master/drive.sh) : Automation script for the drive encryption


1- dmesg | grep -i scsi =>> to get the drive = sdd [DRIVE]

2- ./cookpw.py THEPASSWORD >password.bin =>> THEPASSWORD = your passcode

3- Install 'sg3_utils' package for your distro depends on the distro you use !

4- sudo sg_raw -s 40 -i password.bin /dev/sdd c1 e1 00 00 00 00 00 00 28 00
