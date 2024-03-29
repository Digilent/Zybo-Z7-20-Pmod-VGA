Zybo Z7-20 Pmod VGA Demo
==============

**Note:** The demo contained in this repository has been moved and this repository is no longer being actively maintained. Check out the [Zybo Z7 Pmod VGA demo](https://digilent.com/reference/programmable-logic/zybo-z7/demos/pmod-vga) page on Digilent Reference for more information.

Description
--------------
This project is a Vivado demo using the Zybo Z7-20's, Pmod Ports and the Pmod VGA written in VHDL. The Pmod VGA is controlled by the Zybo Z7-20 through Pmod ports JC and JD. When programmed onto the board, a bouncing box and many test pattern bars are displayed on a connected VGA monitor. The screen resolution is configurable through HDL code.

You may want to change the display resolution if your VGA monitor does not support 1080p, or you want to modify the demo for a specific application. 
To select a different display resolution, select the appropriate set of Sync Generation constants for your target resolution from the list starting at line 47 of top.vhd. Uncomment the ten corresponding constants, FRAME_WIDTH through V_POL, and comment the default versions of those same constants. The default resolution is 1920×1080 @ 60Hz.
Next, select Project Manager in the Flow Navigator. In the Hierarchy tab of the Sources box, expand top under Design Sources and double click on clk_div_inst. Change the clk_out1 requested frequency to the required pxl_clk frequency specified in the selected resolution's Sync Generation comment block. Select Ok, then Generate in the Generate Output Products dialog that pops up. To reprogram your board with the new hardware, return to Step 2.


Requirements
--------------
* **Zybo Z7-20**:To purchase a Zybo Z7-20, see the [Digilent Store](https://store.digilentinc.com/zybo-z7-zynq-7000-arm-fpga-soc-development-board/)
* **Pmod VGA** To purchase a Pmod VGA, see the [Digilent Store](https://store.digilentinc.com/pmod-vga-video-graphics-array/)
* **Vivado 2018.2 Installation**:To set up Vivado, see the [Installing Vivado and Digilent Board Files Tutorial](https://reference.digilentinc.com/vivado/installing-vivado/start).
* **MicroUSB Cable**
* **VGA Monitor**
* **VGA Cable**
 
Demo Setup
--------------
1. Download and extract the most recent release ZIP archive from this repository's [Releases Page](https://github.com/Digilent/Zybo-Z7-20-Pmod-VGA/releases).
2. Open the project in Vivado 2018.2 by double clicking on the included XPR file found at "\<archive extracted location\>/vivado_proj/Zybo-Z7-20-Pmod-VGA.xpr".
3. In the Flow Navigator panel on the left side of the Vivado window, click **Open Hardware Manager**.
4. Plug the Zybo Z7-20 into the computer using a MicroUSB cable.
5. In the green bar at the top of the Vivado window, click **Open target**. Select **Auto connect** from the drop down menu.
6. In the green bar at the top of the Vivado window, click **Program device**.
7. In the Program Device Wizard, enter "\<archive extracted location\>vivado_proj/Zybo-Z7-20-Pmod-VGA.runs/impl_1/top.bit" into the "Bitstream file" field. Then click **Program**.
8. The demo will now be programmed onto the Zybo Z7-20. See the Description section of this README to learn how to interact with this demo.

Next Steps
--------------
This demo can be used as a basis for other projects, either by adding sources included in the demo's release to those projects, or by modifying the sources in the release project.

Check out the Zybo Z7-20's [Resource Center](https://reference.digilentinc.com/reference/programmable-logic/zybo-z7/start) to find more documentation, demos, and tutorials.

For technical support or questions, please post on the [Digilent Forum](https://forum.digilentinc.com).

Additional Notes
--------------
For more information on how this project is version controlled, refer to the [Digilent Vivado Scripts Repository](https://github.com/digilent/digilent-vivado-scripts)


