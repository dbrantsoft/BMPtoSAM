# BMPtoSAM
Converts windows BMP file to a Format the SAM Coupe can understand

Introduction

This program is used to convert a BMP file (24bit or 8bit) of any size into a format that will work with a SAM Coupé. Main use is so you can draw graphics on a PC/Mac etc. for use on the SAM Coupé. 

Converts colours to 7bit and makes a palette of 16 colors from the most used colours. You can also set a starting palette of colours you need (very useful for games that need fixed colours)

With photos it's best on the PC to convert to Web216 colour system.

To run the program you will need Java setup correctly including Path Environment Variable.

In Command Prompt find the path of the program and type the following to run the program, which displays the help screen.


java -jar bmptosam.jar 

Switches to use with the program are:-


-l [filename]  BMP file to load. 
-s [filename]  File name and path to save the image to.  
-sc Saves the Screen as a standard SAM coupe screen format. This has not been tested. Default is off.  
-pal [list]  set starting palette 'n' means free to use/change i.e. 5,n,n,n,n,127
 this would set 0 to 5, 1 to 4 free and 5 to 127. 6-15 also free.  
-br [number]  Increases each original RGB value before convertion. This will brighten or darken the image. This can get a better colour match.  
-nc Gives a different convertion. Instead of stripping off the lower 5 bits, it works out what 3 bit colour closest to real colour.  
-sa [scale]  Coverts to a scale grey, red, green, purple, red-yellow, true-grey. True grey only uses 8 colours of grey.  

The program displays the name of the file it is converting, BMP image type, the actual converted palette, Number colours found, Converted Palette, Used Palette, width and height, Saving file name, Saving mode.

Once the file is converted displays the image in converted state.

File format


width word 
Height word 
colours used  byte 
palette byte*16 
image data    

Sam Disk Image

In the "screenViewer.mgt" image file there is a program to view your images, just boot the disk image in simcoupe and it will auto load. Once you have loaded the screen/image use a mouse to scroll. Click the mouse to exit viewing.

Use an image program to save you images to the sam disk like SamDisk by simon owen. 

