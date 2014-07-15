android_manifest
================

Buidling instructions for Sony Xperia P/U/Sola/Go(nypon/kumquat/pepper/lotus)

mkdir pa;

repo init -u git://github.com/AndroDevLinux/android_manifest.git -b aospa-kitkat;

repo sync;

# Dhcpd rules needed by Wi-Fi Direct
curl https://raw.githubusercontent.com/CyanogenMod/android_hardware_qcom_wlan/cm-11.0/qcwcn/config/android_dhcpcd.conf > device/sony/montblanc-common/config/dhcpcd.conf

# APNs list
curl https://raw.githubusercontent.com/CyanogenMod/android_vendor_cm/cm-11.0/prebuilt/common/etc/apns-conf.xml > device/generic/goldfish/data/etc/apns-conf.xml

#For Xperia P- 
./rom-build.sh nypon;
#For Xperia U- 
./rom-build.sh kumquat;
#For Xperia Sola-
./rom-build.sh pepper;
#For Xperia Go- 
./rom-build.sh lotus;
