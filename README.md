# Megasquirt-Microsquirt-7-LCD-digital-dashboard-for-under-50-DIY-
How to build a 7 inch LCD digital dashboard for cheap, displaying many ECU parameters in realtime 


Do you wish you had money to invest for all these nice and expensive LCD race dashboards out there? Do you need to monitor your ECU Data without bringing your laptop with you all the time?

There's a solution, and it's very cheap. I've been tinkering for years to develop this solution, wasted a lot of money on development boards all for having the BEST solution ever. This is the solution with a wider screen (7 inch). If you prefer 5" screens, check my other repos.

Check the following youtube video to see a demo for the free version: https://youtu.be/rjETbBOaq9w?is=f5A8JH6c0yH7SYUK

On this video, the dashboard is receiving simulated data over CanBus. The firmware is tested and currently running on 20+ cars and it's actually bug free.

Here how you can do it, it's very simple, first you purchase this (if you want to buy me a beer, purchase it through my link:

https://www.waveshare.com/esp32-s3-touch-lcd-7.htm?&aff_id=155489

you need the touch version with 800*480 resolution.

Get a USB Type C data cable and hook it up into your device.

Download my free_bin here: 
https://github.com/somahex00-web/Megasquirt-Microsquirt-7-LCD-digital-dashboard-for-under-50-DIY-/blob/main/Dash_Micro_LCD7_Free.bin

Then visit this website https://esptool.spacehuhn.com/ and connect to your device.

You need to select your board from available COM Ports. It's easily detectable as it says "ESP32" or something recognizable.

If it doesn't connect, hold boot button, hold now reset button, keep for 2 seconds then release reset, wait 1 second and also release boot. It should work now.

After connection you will be prompted what to flash and where. You need to flash the firmware "LCD_DASH_7Inch_FREE.Bin" right at 0x0000 address. if you prefer a more visual guide, check:

https://github.com/somahex00-web/Megasquirt-Microsquirt-7-LCD-digital-dashboard-for-under-50-DIY-/blob/main/How%20to%20flash.pdf

After it's done, reboot the device using the reset button or unplug/plug back your USB.

Very important!!! behind the board there's a small selector to enable the canbus termination resistor. If your canbus doesn't have any other node except ECU and Dashboard, you need to switch it on. if you have other nodes, I suggest you to check with a Multimeter if there are already 60ohm between CanH and CanL wires, this would mean the network is correctly terminated. If there are 120ohm, you most likely have 1 termination only and you need to activate the switch on the board.

Now onto the wiring of the unit to the microsquirt! Follow this:
note: to power the board with your car voltage, you need a 12-24/5v buck converter like the one shown in the following guide: (I prefer the one with USB output, then use a USB cable to power the dashboard. it has proven to be the most reliable setup with 0 failure up to today).

https://github.com/somahex00-web/Megasquirt-Microsquirt-7-LCD-digital-dashboard-for-under-50-DIY-/blob/main/Dashboard%20for%20microsquirt%20installation%20guide%20-%207%20inch%20dash%20ENG%20071125.pdf

I've made tons of better graphics which i'm keeping for licensed use, you can check some on my youtube channel: https://www.youtube.com/@alfredodimatteo2850

One of the most recent version is the following: https://www.youtube.com/watch?v=xfOAbD9B4jw

List of features and available backgrounds here: 

https://github.com/somahex00-web/Megasquirt-Microsquirt-7-LCD-digital-dashboard-for-under-50-DIY-/blob/main/Catalogue.pdf

How to purchase:

premium licensed software price is only 75 Euro, that's a contribution to my years of developing: this will help me to build new units / tools / graphics.

Basically, after you first flash the demo version of the device, you can get an unique license code clicking on the bottom right corner of the screen. If you wish to purchase the paid version, you need to send me license code and send me an inquiry through my website: https://somahex00.wixsite.com/home/contact what you get is your custom licensed firmware bin that will run only on your board and you cannot distribuite it to other boards. This is done to prevent multiple units having the same paid license.
