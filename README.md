# linaro_android_clone_manifest

##Download the Source Code
```
repo init --no-repo-verify -u https://github.com/yinquan529/linaro_android_manifest.git
repo sync
```

##Build the System
```
export CPUS=`grep -c prcoessor /proc/cpuinfo`
export TOOLCHAIN_TRIPLET=arm-linux-androideabi
export WITH_HOST_DALVIK=false
export TARGET_TOOLS_PREFIX=prebuilts/gcc/linux-x86/arm/arm-linux-androideabi-4.9-linaro/bin/arm-linux-androideabi-
source build/envsetup.sh
export TARGET_PRODUCT=pandaboard
make -j${CPUS} boottarball systemtarball userdatatarball
```
