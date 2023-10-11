# disable-device-mgmt
How to disable corporate device management (not for disabling the school DMA or anything)

stuff needed:
- another computer that has admin
- usb drive

## 1. Download iso and flash
on the computer with admin, download the iso file from here https://www.hirensbootcd.org/

![image](https://github.com/seanLimWeiRen/disable-device-mgmt/assets/113512088/3b4d60fa-490b-4d3e-881a-881fdca2bf8f)

download iso2usb.exe

![image](https://github.com/seanLimWeiRen/disable-device-mgmt/assets/113512088/e7827fb9-5a46-4bab-81c3-e399df370c0b)

make sure both files are in same directory
run ISO2USB.exe and run as admin

![image](https://github.com/seanLimWeiRen/disable-device-mgmt/assets/113512088/f5fbf3af-c63f-4a13-b08a-c4eb187c0734)

make sure correct usb drive is selected and correct iso file is selected, then press process

wait for about 5 minutes

done

## 2. Getting bitlocker keys
go to https://aka.ms/aadrecoverykey

get the bitlocker key for the device

write it down somewhere

## 3. uefi stuff
go into uefi

set supervisor password

![image](https://github.com/seanLimWeiRen/disable-device-mgmt/assets/113512088/76b6c774-ed9d-44b1-a5f3-09202c439906)

disable secure boot

![image](https://github.com/seanLimWeiRen/disable-device-mgmt/assets/113512088/3d752a45-6be9-42fc-b307-07b17c3126b3)

enable f12 boot menu

![image](https://github.com/seanLimWeiRen/disable-device-mgmt/assets/113512088/8cb349b9-818a-4712-bd30-5762c65cf854)

f10 to save and exit

## 4. unlocking
turn on the laptop and spam the f12 key until the menu pops up

plug in the usb drive

boot into HBCD (might take some time

open file manager, double click on the encrypted drive and enter the bitlocker key from step 2

press windows key and search for Lazesoft Password Recovery and open it

follow instructions given

![image](https://github.com/seanLimWeiRen/disable-device-mgmt/assets/113512088/f76a1dbf-b8d0-48bf-a884-0eafcb559ff0)

reset the password of a local admin account

restart the laptop and go back to uefi

re-enable secure boot

done

