# Rode NT-USB Firmware Fix

This repository contains, preserves, and backs up the content of the [Reddit post](https://www.reddit.com/r/rode/comments/1avhtdf/fixing_rode_nt_usb_problem_not_recognized/) which provides a solution for the Rode NT-USB problem where the device is not recognized.

## Files

- `Config6400.exe` and its associated DLLs located in the `/Config6400` directory.
- `RODE NT-USB.bin`

## Instructions

1. Download the repository files.
2. Navigate to the `/Config6400` directory.
3. Run `Config6400.exe`.
4. Follow the instructions provided in the Reddit post to apply the firmware fix using `RODE NT-USB.bin`.

### Reddit Post Content
[u/Upper-Farmer4925 originally posted this solution on Reddit including a link to the](https://www.reddit.com/r/rode/comments/1avhtdf/fixing_rode_nt_usb_problem_not_recognized/) - [Config6400.zip](Config6400.zip)

#### Fixing RODE NT USB problem (not recognized)

The problem is that the firmware on the cm6400 chip inside was deleted, which is why my (and many people here) micro is not recognized. It's pretty easy to copy and It will take no more than 5 minutes.

You need to download and open this program: https://www.mikethetech.com/files/Config6400.zip

In VID write 19f7 (which means company id - RODE), and in PID 0003 (means model, in this case - rode nt usb)

Then "connect"

And then click on EEPROM -> FILE to copy the firmware to the computer

To fix broken firmware you need to take steps 1 and 2, but in 3 instead of EEPROM -> FILE you need to select FILE -> EEPROM and select file from comments then don't touch the program until it tells you that you can disable the micro, then disable it and voila connect again and its works, you don't need to buy a new one

----
#### HID Device Error
[u/AlexUwU02 provided a solution for the HID device error](https://www.reddit.com/r/rode/comments/1avhtdf/comment/l9ivfut/)

FOR ANYONE HAVING THE ISSUE OF "cannot find HID device !!!"

Open Device Manager

Under 'Audio inputs and outputs', right-click the USB Advanced Audio Device then click 'properties'

Go to 'Details' and in the 'Property' drop down menu, scroll down to 'Last known parent'

Input the 4 characters after VID and PID into Config6400 (Mine were VID - 0D8C, PID - 016C. (Your values may differ so check under Last known parent just to make sure you use the correct ones)).

Click connect then upload the .bin using FILE -> EEPROM

----
#### Firmware Details
[u/Upper-Farmer4925 provided the firmware file](https://www.reddit.com/r/rode/comments/1avhtdf/comment/kselvx4/) - [RODE NT-USB.bin](RODE%20NT-USB.bin)

FIRMWARE

https://drive.google.com/file/d/19zGgpdTPAYnROIQFBK57mc_03V_71jXb/view

I bought another nt-usb microphone and made a backup from it

UPD: If your micro recognize like "usb-hub" or something different, but NOT Advanced Audio Device - plug it in USB 2.0 instead of Type-C or USB 3, and repeat

## Thanks

Special thanks to u/Upper-Farmer4925 (https://www.reddit.com/user/Upper-Farmer4925/) for providing the solution and the firmware files as well as u/AlexUwU02 (https://www.reddit.com/user/AlexUwU02/) for the additional information on the HID device error.

## Disclaimer

This repository is provided as-is without any guarantees. Use at your own risk.
