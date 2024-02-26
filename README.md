# TWRP Device Tree for Samsung Galaxy S20 Series

The Galaxy S20 Series (codenamed _"x1s"_,_"y2s"_,_"z3s"_) is a family of flagship smartphones from Samsung.

They were announced and released in March 2020.

This device tree is compatible with all 5 devices: S20 4G, S20 5G, S20+ 4G, S20+ 5G, S20 Ultra.

## Device specifications

| Feature                      | Specification                                                                      |
| ---------------------------: | :----------------------------------------------------------------------------------|
| Chipset                      | Exynos 990/9830                                                                    |
| CPU                          | Octa-core (2x2.73 GHz Mongoose M5 & 2x2.50 GHz Cortex-A76 & 4x2.0 GHz Cortex-A55)  |
| GPU                          | Mali-G77 MP11                                                                      |
| Memory                       | 8GB/12GB/16GB RAM                                                                  |
| Shipped OS                   | Android 10 (One UI 2.0)                                                            |
| Storage                      | 128GB / 256GB / 512GB (UFS 3.0)                                                    |

## Kernel source 

Available at [https://github.com/ExtremeXT/android_kernel_samsung_990/](https://github.com/ExtremeXT/android_kernel_samsung_990)

## Bugs

- ADB when MTP is disabled
- /data decryption in OneUI (works on AOSP)

## FBE Decryption
The default branch has FBE disabled because it's only functional on AOSP, for that version, please visit [the decryption branch](https://github.com/ExtremeXT/android_device_samsung_x1s/tree/decryption).

## How to build

This device tree was tested and is fully compatible with [minimal-manifest-twrp](https://github.com/minimal-manifest-twrp/platform_manifest_twrp_aosp).

1. Set up the build environment following the instructions [here](https://github.com/minimal-manifest-twrp/platform_manifest_twrp_aosp/blob/twrp-12.1/README.md#getting-started)

2. In the root folder of the fetched repo, clone the device tree:

```bash
git clone https://github.com/ExtremeXT/android_device_samsung_x1s.git -b android-12.1 device/samsung/x1s
```

3. To build:

```bash
. build/envsetup.sh
lunch twrp_x1s-eng
mka recoveryimage
```

## Copyright

```
#
# Copyright (C) 2024 The TWRP Open Source Project
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#      http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.
#
```
