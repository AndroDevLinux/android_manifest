android_manifest
================

Buidling instructions for Moto G cm-11.0 stable builds

mkdir cm-11.0

cd cm-11.0

repo init -u git://github.com/AndroDevLinux/android_manifest.git -b stable/cm-11.0-falcon;

repo sync;

. build/envsetup.sh;

lunch cm_falcon-userdebug;

mka bacon;
