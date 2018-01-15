## TWRP device tree for Xiaomi Redmi Note 3 (kenzo)

Add to `.repo/local_manifests/kenzo.xml`:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<manifest>
	<project path="device/xiaomi/kenzo" name="android_device_xiaomi_kenzo" remote="TeamWin" revision="android-8.0" />
</manifest>
```

Then run `repo sync` to check it out.


To build:

```sh
make clean
. build/envsetup.sh
lunch omni_kenzo-userdebug
make recoveryimage -j16


Kernel sources are available at: https://github.com/LineageOS/android_kernel_xiaomi_msm8956
