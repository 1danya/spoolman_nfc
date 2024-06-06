## Assembly Instructions

### Step 0: Before you begin
Please read the instructions to the end before you begin.

you might want to print the *test piece*. afterprinting, try and insert the wires in all the grooves; if it is too hard, you should redo your PA and flow rate (orca tests are great)

### Step 1: Printing the parts
print all the files *bottom, lid, button cap* (for a nice effect, print the button cap in a different color).
put the *button cap* in the hole of *bottom*, and cover it with the button itself. the button should be flush, and you should be able to push/activate it by pressing with your finger, but should not wobble/move around

while at it, flatten the legs of the button, and cut them as following: (image)


### Step 2: inserting the LED
get a marker, and mark the gnd of the led (the longest leg). now, with a pair of clippers, cut all the legs flush (about 10mm). now, bend them at 90*, leaving about 5mm straight. insert the led in the *bottom*

### Step 3: Inserting the wires
cut two 20 cm of ftp/utp cable; remove the insulation (carefull at the tin foil, if you are using ftp), and then get the individual wires. separate them, but be gentle, since the cables are very fragile. you should have 16 pieces of 20cm cables. we will be using 15 wires of different sizes, so it is more than enough.

now insert the wires as in the following diagram (image); you should put the wires that go in the pcbs first, because you want to be as precise as possible with them. 
strip about 10mm of the end of the wire, and insert the wire into the groove. you can use a guitar pick or a pair of sharp tweezers (CAREFUL NOT TO POKE AND RUIN THE WIRE); you don't need to push it all the way, just make sure it holds firmly. the beginning of the insulation (at the end where you stripped the wire; at the pcb part) should be flush with the groove (image)

you want to have about 10mm of wire sticking out of the grooves at the end.

after you have inserted all the wires, get the marker and mark the point where the (unstripped) wire is flush with the groove. carefully strip the wires, just below the mark (images)

get the 4k7 (4.7k) ressistor, bend its legs and then insert it in the slot


### Step 4: placing the pcbs
straighten the pcbs wires, and using the tweezers, insert the wires into the pcbs (images)

### Step 5: soldering

first we'll solder the pcbs: straighten the wires, and then solder them on the pcb. CAREFUL NOT TO SHORT THE BOARDS BY HAVING THE WIRES/TIN TOUCH. 
next is the led: if you want, you can use a pair of pliers and twist the wire on the led leg to make soldering easy. same with the resistor (and the 3v3 wires) and then with the gnd wires
last step is soldering the button (gnd, d2 and 3v3)
(images after each step)

### Step 6: multimetering (checking for continuity)
get the multimeter, set it on continuity mode, and check for continuity between all the wires, especially between the neighboring ones. also measure the continuity from the pcb to the rest of the board
(image)

### Step 7: SPOOLMAN
follow this tutorial, and install spoolman on your device
https://github.com/Donkie/Spoolman (do smt nice with the link)
now go to moonraker.cfg, and add the following part:
[spoolman]
server: spoolman adress (aka ip adress, eding with :7912)
sync_rate: 5

### Step 8: finishing the build
after you are absolutelly sure that everything is fine with your build, screw the lid and go over to your pc, and prepare to begin the firmware part of this project

### Step 9: flashing the device
in arduino ide, add an aditional board (http://arduino.esp8266.com/stable/package_esp8266com_index.json), and then select the WEMOS D1 MINI LITE board
now let's test the led, by running *code*
if you are getting errors at this step, consider updating the ch340 drivers (https://www.wemos.cc/en/latest/ch340_driver.html ; https://www.youtube.com/watch?v=BUKe0LfNxnw ; https://learn.sparkfun.com/tutorials/how-to-install-ch340-drivers/all), and make sure you are using the correct port. i recommend uninstalling and installing the drivers

if it the led doesn't blink in the correct order (add order good sir), you should check again the continuity between wires

now it's time to install the libraries (timer, mfrc522, ezbutton). now load up *code*, and replace the following parts:

WIFI_NAME your 2.4Ghz wifi network where pi is accessible
WIFI_PASSWORD password
MOONRAKER_URL printer url (better to use ip adress; make sure the adress doesn't end in /)
NEW_SPOOL_FILAMENT_ID (you say)

