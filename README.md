![](../../workflows/wokwi/badge.svg)

# TinyDice

A submission to Tinytapeout, implementing an electronic dice with minimized circuit using the Wokwi interface.

[Explanation of design](https://hackaday.io/project/183938/log/210501-007-tinydice-dice-on-an-asic)

[Architectural background](https://hackaday.io/project/183938-circuit-golf-electronic-dice-edition/log/203107-005-dice3904-8-minimal-transistor-based-dice)

[Wokwi project](https://wokwi.com/projects/341315210433266259)

![grafik](https://user-images.githubusercontent.com/4086406/188271563-668208bf-615a-499b-ac5a-c2e9ddfcdc3d.png)

![grafik](https://user-images.githubusercontent.com/4086406/188271571-0f875f88-c886-4900-8299-8a89badc3fb6.png)



original readme of the template below the line.
---------------------------------------------------------

Go to https://tinytapeout.com for instructions!

# How to change the Wokwi project

Edit the [Makefile](Makefile) and change the WOKWI_PROJECT_ID to match your project.

# What is this about?

This repo is a template you can make a copy of for your own [ASIC](https://www.zerotoasiccourse.com/terminology/asic/) design using [Wokwi](https://wokwi.com/).

When you edit the Makefile to choose a different ID, the [GitHub Action](.github/workflows/wokwi.yaml) will fetch the digital netlist of your design from Wokwi.

The design gets wrapped in some extra logic that builds a 'scan chain'. This is a way to put lots of designs onto one chip and still have access to them all. You can see [all of the technical details here](https://github.com/mattvenn/scan_wrapper).

After that, the action uses the open source ASIC tool called [OpenLane](https://www.zerotoasiccourse.com/terminology/openlane/) to build the files needed to fabricate an ASIC.

# What files get made?

When the action is complete, you can [click here](https://github.com/mattvenn/wokwi-verilog-gds-test/actions) to see the latest build of your design. You need to download the zip file and take a look at the contents:

* gds_render.svg - picture of your ASIC design
* gds.html - zoomable picture of your ASIC design
* runs/wokwi/reports/final_summary_report.csv  - CSV file with lots of details about the design
* runs/wokwi/reports/synthesis/1-synthesis.stat.rpt.strategy4 - list of the [standard cells](https://www.zerotoasiccourse.com/terminology/standardcell/) used by your design
* runs/wokwi/results/final/gds/user_module.gds - the final [GDS](https://www.zerotoasiccourse.com/terminology/gds2/) file needed to make your design

# What next?

* Share your GDS on twitter, tag it #tinytapeout and [link me](https://twitter.com/matthewvenn)!
* [Submit it to be made](https://docs.google.com/forms/d/e/1FAIpQLSc3ZF0AHKD3LoZRSmKX5byl-0AzrSK8ADeh0DtkZQX0bbr16w/viewform?usp=sf_link)
* [Join the community](https://discord.gg/rPK2nSjxy8)
