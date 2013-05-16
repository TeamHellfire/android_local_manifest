android_local_manifest
======================


Make a build directory:

mkdir Andoid (or whatever name you choose)
cd Android (or the name you chose)

To initialize your local repository using the CyanogenMod manifest, use commands like these:

repo init -u git://github.com/CyanogenMod/android.git -b cm-10.1

curl -L -o .repo/local_manifest.xml -O -L https://raw.github.com/TeamHellfire/android_local_manifest/hf-10.1/local_manifest.xml

( or Download: https://github.com/TeamHellfire/android_local_manifest/blob/cm-10.1/local_manifest.xml
    and place it in ~/Android/.repo/local_manifest.xml (or ~/'name you chose'/.repo)



Then to sync up:

repo sync

Need to pull down the prebuilt add-ons for CM:

vendor/cm/get-prebuilts

And finally to build the CM ROM:

. build/envsetup.sh && brunch  cm_d2tmo-userdebug -j8
or
. build/envsetup.sh && brunch  cm_d2att-userdebug -j8
or
. build/envsetup.sh && brunch  cm_d2spr-userdebug -j8


