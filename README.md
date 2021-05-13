
# TWRP device Tree for Symphony Z Mark 3 to build TWRP touch recovery
# it's time to build a TWRP recovery image
Clone minimal TWRP environment
Follow the instruction in this page
https://github.com/minimal-manifest-twrp/platform_manifest_twrp_omni

Remember to clone the correct version of TWRP based on what Android version your phone have! If your phone have Android 8.0, clone twrp-8.0 branch

Move device tree to TWRP sources
Copy working/(brand)/(device) folder to device/(brand)/(device) folder in TWRP sources
Example:

brand name: Symphony 
device codename: ZVIII
Copy working Symphony/ZVIII/ to device Symphony/ZVIII in TWRP sources
Building
Open a terminal with the current dir pointing to TWRP sources root
Then type
. build/envsetup.sh
to initialize the environment

After that, type
lunch omni_codename-eng
where codename is the codename of your phone

If that is successful, type
mka recoveryimage
to build the recovery

If also that is successful, congratulation!
Go to out/target/product/codename/ (codename is your device codename) and you will find your recovery.img
