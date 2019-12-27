# AutoCAD Automated Plotting for Laser Cutting (AAPLC)

An automated script for AutoCAD to perform plotting to PDF for laser cutters  
Tested with AutoCAD 2020. Will not work with LT versions as this script requires AutoLISP

## What this script does

This script converts all color 7 (default layer) lines into fully red (#ff0000) hairline (0.00mm lineweight) lines ready for laser cutting, while converting all other colors into black, which can either be used for engraving or skipped completely within the laser cutter's options.

## Installation

1. Open a new file (or any file) in AutoCAD
2. Key in the `STYLESMANAGER` command to bring up the folder to place the `lasercut.ctb` file inside
3. Place the `aaplc.scr` script file in a convenient location for later use

## Usage

1. Ensure that the `lasercut.ctb` file is installed correctly
2. Move all objects you intend to laser cut within the 600 by 400 mm boundaries relative to the origin
3. Ensure that all objects you intend to laser cut are on the default layer, color 7. Do not put annotations or other things on this layer
4. Ensure that all lines are single lines, with no overlapping lines (this might not be obvious!). **Overlapping lines will cause double cuts in the machine and may result in a fire.**
5. Run the script by dragging and dropping the script into the current CAD window with your design active
6. Inspect your PDF once the plotting is complete. The PDF is automatically saved to the same folder as your DWG with a "LASERCUT-" prefix and a timestamp suffix
