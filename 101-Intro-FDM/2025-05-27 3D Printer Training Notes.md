# Musings

have people download prusaslicer before  
make sure the bench is EQUIPPED ==DUMBASS==  
- isopropyl , paper towels , scotch-brite , filament , spare beds , flash drives  
find model(s) that will print fine , and model(s) that need support  
install prusaslicer on my other computer and put in Beginner Mode so I can get used to the UI  
3d printing is melting plastic , immediately cooling it so it stays where you put it , then putting more plastic on top of it , over and over again  
cover what an 'overhang' is  
3d printer has two heaters and two fans  
first layer is the most important  
a well adhered first layer keeps the part in place for the rest of the print  
watch the entire first layer before you leave the printer  
prints are weakest vertically  
prints are mostly hollow  `![Screenshot of a comment on a GitHub issue showing an image, added in the Markdown, of an Octocat smiling and raising a tentacle.](./layer-lines-cross-sections)`
prints are not waterproof  
prints are never food-safe 
![[layer-lines-cross-sections.png]]
go over the tools present on the bench  
print failures happen all the time, sometimes they even damage the printer , that's life , but you may be held responsible if it is clear that you failed to follow procedure  
if you put your body or any other object into a moving printer and there is damage , Technocopia is not responsible
show them the "est cost" in prusaslicer

### What we WON'T cover

- making your own 3D models
- printer maintenance
- printing in multiple colors
- printing very large objects
- printing many objects at once

### Rules for the Space

- no printing models for sale
- no prints longer than 36 hours

# Things to Collect

- 3D models
    - one or more "good" models
    - one or more "bad" models that need support : [https://www.myminifactory.com/object/3d-print-rodin-the-mighty-hand-11998](https://www.myminifactory.com/object/3d-print-rodin-the-mighty-hand-11998) (modify this to remove stand pin)
        - SOURCES: [https://www.youtube.com/watch?v=MtNqZ_Rn-xs](https://www.youtube.com/watch?v=MtNqZ_Rn-xs) [https://www.youtube.com/watch?v=kuBbAsnNJFM](https://www.youtube.com/watch?v=kuBbAsnNJFM)
    - one or more "bad" models that are too detailed
- GIFs of good examples of "layers supporting the next" and bad examples

### Things to Purchase

- Gold PETG, 5kg
- Black PETG, 7kg
- White PETG, 1kg
- Scotch-Brite Pads
- 3x fan ==what size fan?==
- power strips
- nippers
- MMU3 auto rewinder kit

# Steps to walk through

- Download and Install PrusaSlicer
- Initial config
    - Printers: MK4S 0.4 , Mini 0.4
    - Filaments: Generic PLA , Generic PETG HF
- downloading and importing a file
    - major websites ( thingiverse , printables )
    - model files vs [ print / sliced ] files
        - why we don't use pre-sliced files -- these can bypass safety checks and damage the machine

# Curriculum

### The Basics

- what is a 3D printer
    - puts plastic down ... yadda yadda
- filaments
    - **PLA** prints easiest but is brittle
    - **ABS** is difficult to print but is very durable
    - **PETG** is the fantastic middle ground
    - **TPU** is the rubbery one
    - Nylon , PET , and abrasives are PROHIBITED
- file types ( STL , STEP , 3MF , obj )
    - I hate 3MF and so should you -- it's an unholy mix of several incompatible data types
- **slicer** takes geometry files and converts them to printer instructions ( **GCODE** )
    - we recommend **PrusaSlicer** because we have Prusa printers , and PrusaSlicer is Open Source , meaning it's safer to use
    - if you use a Bambu Lab printer , Bambu Slicer is a fork ("copy") of PrusaSlicer
        - meaning it has all the same features , but the buttons might be in different places

### The Printer

- tool head and nozzle
    - the nozzle heats up to melt the plastic
        - **DO NOT** touch it , **ever**
        - different size nozzles are available , but the standard size is 0.4mm , and that's what we use here
            - **DO NOT** change the nozzle
    - the tool head has two fans
        - one cools the plastic after it leaves the nozzle
        - the other helps control the heater assembly
        - the printers here check automatically that both fans are working , but if you have a printer at home it might not
- bed and plate
    - the **plate** is removable from the bed
        - **do not** print on the bed without a plate
    - the bed **heats** the plate so the plastic sticks to it
    - **gently bend** the plate to release a finished print
    - no glue
        - you may have seen online to use glue stick on the build plate. do not do this. if i find that you did this i will hunt you down and make you eat the glue stick
- homing
    - the printer does not know where its moving parts are until it runs a homing operation
    - once homed , the motors are powered and you **cannot** move the parts by hand
    - the printer will automatically home at the start of each print

### Preparing a File for Printing

- Launch PrusaSlicer
- First Time Config
    - Prusa FFF
        - MK4S with Input Shaping 0.4mm
        - Scroll down for Mini with Input Shaping 0.4mm
- **The Top Bar:** Plater / Print Settings / Filament Settings / Printer Settings
    - As a beginner, you shouldn't leave the **Plater** view, you won't need anything in the other tabs.
- **Simple / Advanced / Expert** -- leave it on Simple
- **The Major Settings**: Printer / Filament / Print Settings
    - I like to go in this order: Printer --> Filament --> Print Settings
- Moving the view: Left Click and drag to orbit , Right Click and drag to move
- import the STL ( Add button / drag it in / File>Import )
- tools: move , rotate , scale , place on face , auto arrange ==(come back and verify these are the right names)==
- set the orientation
    - in most cases the largest flat face goes on the bed
        - 'auto select face' can do that for you
    - in all cases , try to minimize the amount of overhang
- adding support
    - ==for the hands-on portion, use a model where auto support works==
- for common mistakes the software will alert you in the corner of the screen
    - ==do i want them to encounter an alert in the hands-on ? no , right ?==
- click "Slice now"
- prepare vs preview
- previewing the print - ==what to look for==
- export to USB (and eject)

### Preparing the Printer

- adding/changing filament
    - ==show the 'change' process , not the 'add' process==
    - spool holder and feeding tube
    - Change Filament procedure
        - selecting the temperature
        - purging
            - 'Purge More'
            - wait a few seconds and it will be cool enough to grab with your fingers
- ##### The Pre-Flight Check
    
    - verify the nozzle is clean -- gently brush it if necessary
    - verify the steel plate is present and clear
    - grab a paper towel, squeeze a small amount of isopropyl onto the plate, and wipe the plate
- insert USB -- it should automatically show the file you just exported
- verify the filament on screen matches what's loaded ==(what else does the screen show?)==
- press Print
- wait for the entire first layer to finish before walking away
- ##### Pause , Stop , Emergency
    
    - **Pause** and **Stop** are located on the screen
        - You can pause a print to change filament
        - Stop the print if the print has failed.
        - If you see someone else's print failing, please pause or stop the print.
    - In an emergency , the Reset button instantly halts the machine
    - In the event of a fire (extremely unlikely) the fire extinguisher is on the **left side** of the 3D print bench. Pull the pin, aim the hose, squeeze the handle.

### After Printing

- wait until the printer has fully stopped moving
- lift the plate from the bed
- flex the plate to release the print
- clear ALL plastic from the plate
- return the plate to the printer -- align with the pins

### The Test

-