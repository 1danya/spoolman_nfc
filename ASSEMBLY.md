## Assembly Instructions

### Step 0: Before you begin
- print test piece
- link to Ioans build log

### Step 1: Print STLs
> Tip: Please make sure your printer is properly calibrated (especially PA and flow rate) as it is critical to get correct grooves for wires.

> Tip: You can use any kind of firm filament from PLA to ASA.

> Tip: Print all STLs with default positioning without any supports. Button cap is "turned upside down" in STL so that the visible part is printed on the first layer.

Print [FRONT_COVER_beta.STL](/STLs/nfc_spoolman_FRONT_COVER_beta.STL) and [BUTTON_CAP_beta.STL](/STLs/BUTTON_CAP_beta.STL) first. Put your button cap in its hole and cover it with button like shown in the picture:

![](/img/button_in_place.png)

Firmly hold the back side of the button with your finger and try to press the button cap from the other side. You should be able to push it but it should not wobble around.
If you can't properly press it or it wobbles around, reprint button cap with a different scale. **Button cap should be flush with the outer surface! It should be not very easy to push by design, because using it involves dangerous operations such as heating your nozzle and pausing the print process.**

You would also need to print the [BACK_SIDE_beta.STL](/STLs/BACK_SIDE_beta.STL), but it can be done at any point of the build.

### Step 1: Laying down the wire
> Tip: Make sure you are using UTP/FTP with a solid core wire. Stranded might work too, but it would be much less convinient for you.

Cut two 20cm pieces of the FTP/UTP cable, carefully remove insulation, foil (if FTP) and uninsulated copper wire. Separate the pairs, but remember to be gentle with it, you don't want to break the wire inside the insulation. You should have 2x4x2=sixteen 20mm pieces by stripping two cables.

This is what you want to end up with, in total you should use 15 wires of different size. All of them are shorter than 20mm and because of that you'll reuse some of the pieces:

![](/img/wiring.png)

> Note: Number "3" and "4" represent the amount of ends that meet in this point

First you wanna put all the wires that would go into the PCBs because you need to be extra precise with how they are positioned. Strip one end of the 20cm piece (you want to have around 10mm of the naked wire) and insert the wire into the groove.
Carefully poke it with sharp tweezers to make it go inside. You don't need to push it all the way, just make sure it holds.
The begging of the insulation **should** be flush with the beginning of the groove:
![](/img/start_of_insulation_and_groove.png)
Don't worry if you are not 100% precise just now. You will fix it later when you'll putting the PCBs in.
