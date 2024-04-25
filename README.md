This is a compiled .bin Bootloader file for Prusa MINI/MINI+ Buddy boards.

This might be useful if you bricked your board somehow and need to go back to stock firmware.
In my case, I've had my printers running on Klipper firmware and after some time I wanted to go back to the original firmware.
I had some problems going back and it took me some time to do so, so I hope this repository will help you.

- Appendix on your Buddy board must be broken, if you're reading this it probably is but I just wanted to mention it anyways.
- All you'll need is a Micro USB cable, a USB drive and STM32 Cube Programmer installed on you computer.

- Make sure you have some old USB drive, I tried 5 different ones and only one worked.
- It has to be formated in FAT32 and the one that worked was some old/slow 4Gb drive

Recovery steps:

1. Remove the Buddy board cover and brige the two pins for recory mode
2. Connect the buddy board to your computer with a micro USB cable and turn ON the printer
3. Inside STM32 Cube Programmer, open file, select the bootloader file from this repository
4. Download the file onto the MCU
5. Reboot printer
6. At this point, you should get an error on the MINI Display telling your that there is no firmware file and that you should load it over the USB drive
7. Find Firmware 4.4.1 on Original Prusa Buddy board firmware repository and put both files on you USB drive (This step will update the bootloader)
8. Flash the 4.4.1 firmware by plugging the USB drive into the printer and pressing the reset button, following the steps on screen
9. From here, you can either do the first time setup or upgrade to newer firmware but at this point your printer should be restored!

