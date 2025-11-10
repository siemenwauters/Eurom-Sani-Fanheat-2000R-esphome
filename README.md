To give the bathroom that extra boost in temperature when the woman of the house gets ready i needed a smart controlled heater that i could control from home assistant. 
Quickly it became clear that there is not really any decent wall heaters that have a wifi intergration other than some that use some non standard version of tuya.

Since those already cost a lot more just to add the wifi functionality to the heater i went on a path to build my own. The first attempt with a ir led to control a heater worked but was not relyable enough to my teste.
When i found a little heater that comes from a decent brand popped up on a local second hand site i jumped for the opportunity to get it at 15 euro since i did not need the warranty anyway with my modifications.

Below is a picture of the end result

![IMG20251110152738](https://github.com/user-attachments/assets/93db5172-29ec-47eb-8243-870329bf06fd)

if you want to replicate this project you might have to do a little work of your own but i can give you the bulk of the needed information.

When you open the heater ( there is also 2 screws underneath the 2 rubber feet on the wall standoffs ) you will find that the electronics consist of 2 boards. 
The board in the front that handles logic , IR receiver status indication etc. The other board controls the relays and the fan.

The good news is that the interface between these 2 boards is so simple that we can simply replace the complete control module with the esp32 and a relay board ( you could use something else, relays are just simple to keep things separated )

The parts i used are these: ( you can use other variations i will add some info why i picked these )
relay board : https://nl.aliexpress.com/item/1005003571799820.html?spm=a2g0o.order_list.order_list_main.59.21ef79d2hXhZN2&gatewayAdapt=glo2nld ( needed a board that worked with the esp 3.3V )
ESP32C6 : i got the esp32c6 since i got these when i wanted to try and make a zigbee device. this was not simple enough compared to esphome so i switched halfway trough the project. Another esp will work as long as you change the pins but the antenna connector is usefull.
PCB's : https://nl.aliexpress.com/item/1005008177952205.html?spm=a2g0o.order_list.order_list_main.149.21ef79d2hXhZN2&gatewayAdapt=glo2nld i got the 4x6 ones. i had to make the holes a bit larger anyway so any board will work with some changes.
usb module: https://nl.aliexpress.com/item/1005009204958739.html?spm=a2g0o.order_list.order_list_main.125.21ef79d2hXhZN2&gatewayAdapt=glo2nld i received a comment that this module is not relyable so use it at your own risk. it is just what i used but anything that is compact and can provide the esp with power will work.

othet than that i got a 2.4ghz antenna, some headers, some cables general purpose stuff basically. 
