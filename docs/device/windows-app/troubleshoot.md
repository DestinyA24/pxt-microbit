# Troubleshooting downloads from the Windows 10 App

Is Windows App not downloading your program properly? Let's try to figure out why!

## Step 1: Check your cable

Make sure that your @boardname@ is connected to your computer with a micro USB cable. You should see a **MICROBIT** drive appear in Windows Explorer when it's connected. 

![MICROBIT drive](/static/mb/device/windows-microbit-drive.png)

If you can't see the drive:

* **Make sure that the USB cable is working.** Does the cable work on another computer? If not, find a different cable to use. Some cables may only provide a power connection and don't actually transfer data.
* **Try another USB port on your computer.**

Is the cable good but you still can't see the **MICROBIT** drive? Hmm, you might have a problem with your @boardname@. Try the additional steps described in the [fault finding](https://support.microbit.org/support/solutions/articles/19000024000-fault-finding-with-a-micro-bit) page at microbit.org. If this doesn't help, you can create a [support ticket](https://support.microbit.org/support/tickets/new) to notify the Micro:bit Foundation of the problem.

## Step 2: Check your firmware version

It's possible that the firmware version on the @boardname@ needs an update. Let's check:

1. Go to the **MICROBIT** drive.
2. Open the **DETAILS.TXT** file.<br/>
![](/static/mb/device/mb-drive-contents.jpg)<br/>
3. Look for a line in the file that says the version number. It should say **Version: \.\.\.**
![](/static/mb/device/details-txt.jpg)<br/>
If the version is **0234**, you **NEED** to update the [firmware](/device/firmware) on your @boardname@. Follow the upgrade instructions described next.

### Upgrade the firmware

1. Put your @boardname@ into **MAINTENANCE Mode**. To do this, unplug the USB cable from the @boardname@ and then re-connect the USB cable while you hold down the reset button. Once you insert the cable, you can release the reset button.

![MAINTENANCE gesture](/static/mb/device/maintenance.gif)

2. You should now see a **MAINTENENCE** drive instead of the **MICROBIT** drive like before. Also, a yellow LED light will stay on next to the reset button.
3. **[Download the firmware .hex file](https://support.microbit.org/helpdesk/attachments/19008095092)**
4. Drag and drop that file into the **MAINTENANCE** drive.
5. The yellow LED will flash while the `HEX` file is copying. When the copy finishes, the LED will go off and the @boardname@ resets. The **MAINTENENCE** drive now changes back to **MICROBIT**.
6. The upgrade is complete! You can open the **DETAILS.TXT** file to check and see that the firmware version changed to the match the version of the `HEX` file you copied.

If you need more information, go to the **[firmware upgrade](https://support.microbit.org/support/solutions/articles/19000019131-how-to-upgrade-the-firmware-on-the-micro-bit)** page at microbit.org.

### ~hint
If you want to know more about connecting the board, Maintenence Mode, and upgrading the firmware, read about it in the [DAPLink on micro:bit](https://www.mbed.com/en/platform/hardware/prototyping-production/daplink/daplink-on-kl26z/) page.
### ~