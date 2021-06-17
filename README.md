# Windows 11

This is the unofficial documentation on how to install Windows 11.

IMPORTANT!!!!
Read the entire documentation before trying anything, as some steps require certain requirements. (Blank disk, if not, wipe one)
We highly recommend you to read EVERY SINGLE LINE for installing Windows 11, otherwise we aren't responsible for the problems you cause.

# Installing
In the first instances, you need to download the .iso file to boot your PC with it in the future!                  
To do this there are many possibilities on the internet, but I have listed the download links I used below.

Download the Windows 11 Beta 21996.iso file [here](https://drive.google.com/file/d/1J6dPZMr5dlZyrrzTTPzaUCeV0yHaZTAk/view).
> Note: `Secure Boot and TPM` must be enabled in Bios (For the above .iso file)!



Download the Windows 11 Non TPM 2.0 Non Bootable.iso [here](https://drive.google.com/file/d/1QGvcjEM_SM1eDnoHYzSxSe9wq_t5Jpsw/view)

## One more installation required! ##

If you have downloaded one of the .iso files that is best for your PC, you need to create a so-called `Bootable USB` that you will start with further in this tutorial Windows 11 installation menu.

To create a 'Bootable USB' you need a program called 'Rufus'
> Rufus is a small application that creates bootable USB drives, which can then be used to install or run Microsoft Windows, Linux or DOS. In just a few minutes, and with very few clicks, Rufus can help you run a new Operating System on your computer.

Download Rufus [here](https://rufus.ie/)

## Creating the bootable USB ##

Now it is finally time to start the real thing, because we now have to make a bootable USB in rufus, to do this you have to open Rufus!

> Note: Most of the time 8 GB is enough, 16 GB is guaranteed to be enough (This is for the USB we will be using)
>> !!! Important: All data you have on that USB will be deleted when you make a bootable USB, so we advise you to make a backup of it, or put it on another PC / USB!

Now open the program called `Rufus`, then click `Yes`

![image](https://user-images.githubusercontent.com/50002439/122442166-90706700-cf9e-11eb-8582-f4fa6b92e681.png)

Now it should look something like this.

![image](https://user-images.githubusercontent.com/50002439/122442250-aa11ae80-cf9e-11eb-8498-2f9cd4fbb3f2.png)
> Note: On the screenshot my disk (USB) is already selected
> I've already inserted the USB (Which I recommend doing before opening the program)

Then you click button which says: `Select` and then select your .iso file

![image](https://user-images.githubusercontent.com/50002439/122442822-4471f200-cf9f-11eb-8c57-11980a822be1.png)
![image](https://user-images.githubusercontent.com/50002439/122443010-72efcd00-cf9f-11eb-9707-5c51bf858399.png)

> Again: To mention it again, these settings have helped me, and can sometimes differ per computer, if you don't know how or what, I advise you to ask an expert, expert, experienced, or just to to search
Now click on the button: `START` and wait for it to finish. (I'm not doing this now as I've done this before)

## Booting via the USB ##

After we have done all these steps it is finally time to boot the disk via our bootable usb, to do this you will always need an empty disk (if this is not possible you will have to wipe one), this can be done too can be done via the boot menu itself but this is also possible

I used an `HP EliteBook Folio 9470m` for this experiment
Therefore, the following boot shortcuts may not match other laptops not made by HP

### First start you computer, and spam the hotkey `ESC`, until it opens this little menu

![image](https://user-images.githubusercontent.com/50002439/122444669-155c8000-cfa1-11eb-8dff-a0df2179d254.png)

![image](https://user-images.githubusercontent.com/50002439/122444664-12fa2600-cfa1-11eb-8acf-f2bbc8cb5125.png)
