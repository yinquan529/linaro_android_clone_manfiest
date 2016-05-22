# linaro_android_clone_manifest

##Download the Source Code
```
repo init --no-repo-verify -u https://github.com/yinquan529/linaro_android_manifest.git
repo sync
```

##Build the System
```
export CPUS='grep -c prcoessor /proc/cpuinfo'
export TOOLCHAIN_TRIPLET=arm-linux-androideabi
export WITH_HOST_DALVIK=false
export TARGET_TOOLS_PREFIX=prebuilt/gcc/linux-x86/arm/arm-linux-andorideabi-4.9-linaro/bin/arm-linux-andorideabi-
source build/envsetup.sh
make -j${CPUS} boottarabll systemtarball userdatatarball
```
