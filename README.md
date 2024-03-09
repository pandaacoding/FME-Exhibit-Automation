# FME-Exhibit-Automation

## Overview of the tool
This FME tool will get user input on ObjectID for point of the beginning of a line and the last point of the line. This tool will create exhibit maps. If the line cross more than 1 section, it will create .mxd file for each section. Where the GIS user can easily review, adjust location of the annotation, and export to pdf.

## Problem
When GIS user adjusting vertex of where the line cross each section. They have to create a point and get the correct coordinates both in geographic coordinates and projected coordinates. If the line cross 10 different sections. They have to do this at 10 different location. and they have to do it in the same map. If you make mistake on any map, they have to go redo the whole layout view and reexport again.

## Solution
We use python tool box to send database information and get object ID of the first and last point of the main line as well as the feature class of those points. FME will do all the calculation of where the line cross each section. FME will then create the staging GDB with all the info. we then have Python tool box in ArcMap read that staging GDB, and create .mxd for each of the section. GIS users can now go to each basemap file and adjust each one and export them individually. If they mess up on one, they can just go back to that mxd without messing up with the other maps.

## Tools Dependencies
1) FME
2) ArcPy
3) ArcMap

## Example Product
Below is picture of what the workspace looks like in FME.

![Exhibit_automation](https://github.com/pandaacoding/FME-Exhibit-Automation/assets/80724379/6dd4e4a2-84bc-4da1-a4c4-26425e92f8d6)

This is the picture of the product.

![exhibit](https://github.com/pandaacoding/FME-Exhibit-Automation/assets/80724379/ea8567d8-9e7c-45e2-a844-4a2a4274974e)
