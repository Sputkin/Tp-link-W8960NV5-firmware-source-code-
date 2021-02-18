# Tp-link-W8960NV5-firmware-source-code


download link https://drive.google.com/file/d/11WJ8CjQKWqkitMXwSBY5FbCtMtFkUPXT/view?usp=sharing

### step 1 

+ install dependencies
+ NOTE: the whole procedure was tested on a 32-bit ubuntu machine

      sudo apt-get install libncurses5-dev gawk gettext unzip file libssl-dev
      sudo apt-get install flex bison gcc-multilib g++ zlib1g-dev build-essential

+ Decompress the archive with your favorite tool.
+ Use the ./prepare script to install and decompress uclibc and source or do this manually moving the toolchain to / opt.


### step 2      
      
+ cd TD-W8960Nv5.0_consumer 
+ make PROFILE=W8960NV5
+ the images can be found in {ROOTDIR}/images

                                                     
### step 3
      
+ Flash the firmware using Broadcom CFE bootloader https://wiki.openwrt.org/doc/techref/bootloader/cfe
      
   
### NOTE
      
The image produced is fully functional ( including the ADSL(+) part ), some nodes have been modified for the correct startup and the interface of the uhttpd webserver has been modified. You can add new binary and more. To restore the original image, download the right firmware version and then do 
     

## dd if=original_firmware.bin bs=1 of=stripped_firmware.bin skip=512
      
      
![Preview](https://raw.githubusercontent.com/Sputkin/Tp-link-W8960NV5-firmware-source-code-/master/img/wbs.png)


