# Instructions

## Introduction
Here ARE complete instructions for installation and using of MAT_Blinds.

## Basic concepts
- hardware has revision ([rev](../Schematic/))
    - hardware revision = board revision
- software has version ([ver](../Code/))

## Step 1 (choose software)
You will need to select the [software](../Code/) you want to use and choose the [board revision](../Schematic/) that the software supports. (For each software version, it is written which board revision it supports.)

## Step 2 (parts)
You will needs to print a few parts on a 3D printer.
- [bracket for stepper motor](../parts/3D_parts/Bracket_28BYJ-48_v1.stl) Big a shout-out to [John Beale](https://www.thingiverse.com/jbeale/designs) for this proposal.  (only for 28BJY-48)
- [drive wheel](../parts/3D_parts/Drive_wheel/) Big a shout-out to [Martin Bucknall](https://www.thingiverse.com/paraglider_nut/designs) for designing these proposals. 
    - (Each type of blinds need a different one, according to the chain. I used these two because I have two different types of blinds.)

parts list
- 6x - stepper motor (I use [28BJY-48](../Schematic/datasheets/28BYJ-48.pdf))
- power supply - A recommended power supply is written for each [revision](../Schematic/).
- [board](../Schematic/) - which you selected in step 1.
- board case (not for every rev)
- self-tapping screws (for bracket mounting)

## Step 3 (create board)
After selecting the [software](../Code/) and correct [revision](../Schematic/) of the board. The board needs to be made. The entire schema is available for each board. (There are two ways how to make a board. The first one is to buy [daughter board](./daughter_board.md) and just connect them together according to the schema. The second option is to draw the board according to the schema and let them make.

## Step 4 (upload software)
So if we already have a board made, we will need to upload the software we want to use. There are more options for uploading software to the board. I chose the option using „STM32 ST-LINK Utility“ more about uploading [here](../explanations/uploading.md).

## Step 5 (setup board)
After uploading the software, you will still need to set up the board. Each software version has a file named Setup.md. According to it, you will set everything you need.

## Step 6 (congratulations)
If you get this far, the MAT_Blinds project should work for you at home. ❤