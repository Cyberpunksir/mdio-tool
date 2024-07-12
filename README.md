mido-tool is a low-level Android debug tool for communicating with devices attached on MDIO bus. 


Build 
At the moment, copy mdio-tool to Android SDK external folder, configurating Android building environment;
Now build mdio-tool at Android SDK root directory with commands:

# configuarting Android building environment
source build/envsetup.sh

lunch aosp_arm64-eng

or run lunch and you will input combo number
You're building on Linux

Lunch menu... pick a combo:
     1. aosp_arm-eng
     2. aosp_arm64-eng
     3. aosp_blueline-userdebug
     4. aosp_blueline_car-userdebug

Which would you like? [aosp_arm-eng]

# final build command
mmm external/mdio-tool $(nproc)


mdio-tool
=========
This is tool to read and write MII registers from ethernet physicals under Android.
It has been tested with Realtek and Marvell PHY's connected via PCIe and should work
with all drivers implementing the mdio ioctls.

mdio-tool comes with ABSOLUTELY NO WARRANTY; Use with care!

Syntax:
	mdio-tool [r/w] [devname] [addr] <value>
	./mdio-tool w eth0 0x10 0x0
	./mdio-tool r eth0 0x0


