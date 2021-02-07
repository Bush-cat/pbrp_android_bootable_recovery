**Resurrection Remix Recovery <br>**
**Based on PBRP**

You can find a compiling guide here pitchblackrecovery.com/docs/how-to-compile

##init PBRP repo
```
repo init -u git://github.com/PitchBlackRecoveryProject/manifest_pb.git -b android-9.0
```

##change bootable recovery repo to Bushcat (CTRL+X to save, then press Enter to save)
```
nano .repo/manifests/twrp-extras.xml
```
#remove the line:
```xml
  <project path="bootable/recovery" name="android_bootable_recovery" remote="PitchBlackRecoveryProject" revision="android-9.0"/>
```
(CTRL+X to save, then press Enter to save)
```
nano .repo/manifest.xml
```
add the Lines below <manifest>:
```xml
<remote name="Bushcat"
    fetch="https://github.com/Bush-cat"/>
<project path="bootable/recovery" name="rr_pbrp_bootable_recovery" remote="Bushcat" revision="android-9.0" />
```
(CTRL+X to save, then press Enter to save)

#sync
```
repo sync --force-sync
```

Credits:
RR Logo by @bounty780; 
Loading animation by Epicrex; 
PBRP; 
TWRP; 
new Icons and Design made by Bushcat; 

this theme was created by Bushcat
