# OOPrailwaySim
 You must have at least version 1.8 for your assignment, but it is recommended to have he latest version.
## V1.94 5/5/25
fixed bug whereby when a loco was slowed its carriages jumped back and then caught up,
## V1.94 3/5/25 (yes Bank Holiday Weekend!)
fixed bug where carriages behaved erratically when a loco was stopped.
## V1.92 28/4/25
captureVehiclesState(); now also captures state of crossings and resetSImulation() resets to this.
## V1.91 28/4/25
turned debug info off, turn it on with DebugLevel.setLevel(2);
## V1.90 24/4/25
deleteCompleteLoco(locoID) to remove a loco and its carriages from the GameWorld \
deleteCarriage(locoID) to remove the last carriage from a loco from the GameWorld \
fixed crossing issues \
This version is ok to record your demo. \
Please add it to your project.\

## Adding the Jar File IntelliJ
... Open your installed IntelliJ IDEA Project and Go to the File > Project Structure \
Select Modules at the left panel and select the Dependencies tab. \
Select the + icon on the Dependencies tab (the rightmost one) and select 1 JARs or Directories option. \
select OOPRailwaySim.jar. \
Click on the OK button \
Note: It is advised to put the downloaded jar in your project directory and not leave it in a download directory. \ It has been known for other programs, \ such as virus checkers, to move, disable, or delete files in the download directory. \

Note this is SimView, which holds the documentation generated in the main project and the jar file, generated as an artefact in the main project. \