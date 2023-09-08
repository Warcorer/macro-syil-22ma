# Marcos for Syil/Syntec

## Start Here
To use these marcos, follow the steps below:
1. Download and copy the macro(s) to a USB drive.
1. Plug the USB drive into the controller.
1. On the controller, go to `Settings`, `System admin`, `Marco manager`, `Import`.
1. Select the macro(s) and import them into the controller, no reboot necessary.
1. Marcos can be invoked via MDI, e.g., `G65P8000`.
1. Marcos can also be invoked via NC program in auto mode.


## O8000 Unload all tools
Marco to unload all the tools in the machine.

* It will load tools into spindle, and prompt operator to unload the tool.
* Upon unloading the tool, it will update and remove the tool from the tool table.
* Repeat until all the tools are removed.
* Pocket with tool number equal to 0 will assumed to be empty and skipped.

User configuration:
* Certain tools (e.g. probe) can be marked to be skipped.

Known issue:
* When prompted to remove the tool, operator need to switch the machine to JOG/INCREMENTAL JOG/MPG mode in order for the tool withdraw button to be operatable. 
* After unloading the last tool, in order to properly update the tool table, spindle tool number will be set to 0. This will cause a tool changer alarm, which can be safely ignored.