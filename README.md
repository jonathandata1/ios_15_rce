
# iOS 15.0.1 RCE V1 
### Author: Jonathan Scott  @jonathandata1
### Date: October 9th, 2021
[![iOS 15.0.1 RCE V1](https://i.postimg.cc/TY1nSpK9/Untitled-design-Max-Quality-2021-10-09-T015144-437.jpg)](https://www.youtube.com/watch?v=gyHxYlmDKy4&t=1s")


### Release Version 1.0
## Description
### When an iOS device has been connected to a trusted host, or is connected to a trusted host, an attacker can airdrop a website that calls back to a websocket that is able to execute code on the device, transfer data, monitor all actions, even mirror the entire device by using Quicktime. 
## How to run
#### `brew install libimobiledevice`
#### `brew install websocketd`
#### `brew install timelimit`
#### apple configurator 2 > install automation tools, you'll need this to run cfgutil erase
#### Have your device plugged into your computer, if a trust prompt appears press trust

 1. Open index.html and replace 0x.local with your own local host machine - find this on line 219
 2. run ./index.sh
![iOS 15.0.1 RCE V1.0](https://i.postimg.cc/d0HWbzqk/Screen-Shot-2021-10-10-at-2-42-36-PM.png)
 3. You will have a websocket runnning and the JS website should automatically open, you should be using chrome for this PoC as the sharing through airdrop functionality is easy to use. I have tried to make this a simple as possible by the way...
 4. If you don't see the webpage or it doesn't open, you can open chrome browser and go to ex: http://0x.local:8081, and you will see the JS website open up, of course replace 0x with whatever your localhost is...
 5. You can then share this website with the device that you have plugged into your host machine and you can monitor anything that is happening on the device, transfer files, make a backup, and erase the device as well...
 6. ![iOS 15.0.1 RCE V1.0](https://i.postimg.cc/bwY9q3VQ/Screen-Shot-2021-10-10-at-2-45-26-PM.png)
 7. The Javascript is a little funky, I hate web development so if anyone wants to fix the javascript please do lol
 8. You can see that I have bash files that executing everything that is being displayed on the website, i am using libimobiledevice to query, and i'm sure if you're even reading this you can get the point I am making. you can just use Apple's own Apple Configurator 2 for this exploit, you don't even need to install libimobiledevice if you don't want to. 

#### This version of the Raging Colossal Erection uses Airdrop, and the issue is that you can send a website to a device that has been trusted and take control of this device...there is never any prompts that show up on the device at all. 
## NOTE: THIS CAN BE DONE EVEN IF THE PHONE IS LOCKED WITH A PASSCODE, WAKE THE SCREEN SO THAT AIRDROP SHOWS UP AND SHARE THE WEBSITE WITH THE PHONE YOU ARE ATTACKING AND YOU NOW HAVE CONTROL

### If wi-fi sync is enabled on this device you can now execute wireless commands to the device.

### Version 2 of my exploit will be sending this Attack Via SMS and From a Remote Server not a computer on the local network, I will be using ngrok for this.

### it is worth noting that [](https://twitter.com/pfpwnd)

@pfpwnd spoke about file injection...this is for sure a possibility especially if you are already a trusted host...

### To everyone that thinks this is not a big deal...go tell all of the schools, government agencies, corporations, and anyone else who actually has this trusted access of thousands of devices...would someone need to have access to those lockdown files...yes...and your point is??? Should we fire all the IT managers that have access to all the lockdown files in your corporation so that this can't be done? 

### There are "security experts" that are saying this is not an RCE...

### If you can control someone's phone without them knowing and without their approval, it's called a Raging Colossal  Erection, if you can wipe their phone without them knowing or approving its called a raging colossal erection...what is the process that executes on the phone when the phone is wiped? Oh code is executed with the phone is wiped? SMH....



