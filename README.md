# ElegooNeptune3ProMods
This is a journey documenting my first time using github and modding my Neptune 3 Pro


First you will need a Raspberry Pi, most models that are 3b and higher will work fine. To install [klipper](https://github.com/klipper3d/klipper) on your pi go to [raspberrypi](https://www.raspberrypi.com/software/) and download the imager. Plug in a micro sd into your computer with the imager (other storage can work this is just what im using)

While in the imager select
Device: The Pi you have
OS: Other specific purpose --> 3D Printing --> Mainsail OS
Storage: Select the storage device you are using (This will be wiped)
Customization: set your user name and device as you want. I will be setting both as "klipper"

Insert the micro sd into the pi and power it on. It will start the download process, once its dont restart if it didnt already and login. 
  Yay! Your klipper is now ready to boot into, Go to http://klipper.local ( what ever the device name is).


In klipper.local create a folder named "printer.cfg" and paste [this](printer.cfg).

PRINTING

In console enter "BED_MESH_CALIBRATE", you might have to offset the z or level a few times.

find model you would like to print and put it into the slicer of your choice, set the settings how you would normally. Instead of printing, export the gcode and upload into klipper and hit print. you can adjust the speed and extrusion rate in the dashboard for faster prints.
  


