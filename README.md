android_manifest
================

Buidling instructions for Nypon [Sony Xperia P]

mkdir pa;

repo init -u git://github.com/AndroDevLinux/android_manifest.git -b aospa-kitkat;

repo sync;

./rom-build.sh nypon;
