# Опис змін із v2.10

Below is a summary of changes that affect the user interface and/or how EdgeTX functions. It does not cover all bug fixes. For a _**complete**_ list of changes (including bug fixes), please read the release notes.

#### Generally

* Support for next generation radios (based on H5/H7 microcontrollers) which will bring much faster color LCD and black & white radios, with lots more RAM and flash in order to bring new features and functionality ([#5228](https://github.com/EdgeTX/edgetx/pull/5228))
* Can now use `u-blox` native binary protocol (rather than only NMEA) if adding a GPS to your handset ([#4689](https://github.com/EdgeTX/edgetx/pull/4689))
* When editing telemetry sensor ratios, you can also see the percentage value to help give the value meaning ([#4649](https://github.com/EdgeTX/edgetx/pull/4649))
* Update to Lua 5.3 (was previously 5.2) - which saves some RAM, and also allows for binary compatibility with Companion (meaning `.luac` files created using simulator on the PC are now compatible with the handset) ([#4203](https://github.com/EdgeTX/edgetx/pull/4203))
* ELRSv4: Master/CRSF trainer option to use ELRS backpack to relay head tracker data as inputs ([#5724](https://github.com/EdgeTX/edgetx/pull/5724))
* ELRSv4: support for optional arming method that frees up CH5 ([#5641](https://github.com/EdgeTX/edgetx/pull/5641))
* For radios with customizable switches, you can now easily create a virtual 6POS group, as well as have groups of switches - GRx ([#5016](https://github.com/EdgeTX/edgetx/pull/5016))
* Haptic on power on can now be disabled ([#5017](https://github.com/EdgeTX/edgetx/pull/5017))
* Radio can be configured to automatically power off if left inactive ([#3414](https://github.com/EdgeTX/edgetx/pull/3414))
* Sticky logical switch state can be configured to persist across reboots ([#4978](https://github.com/EdgeTX/edgetx/pull/4978))
* USB joystick support for Android game pad functionality ([#4626](https://github.com/EdgeTX/edgetx/pull/4626))
* Even shorter power on/off delay option - 0.5 seconds ([#5134](https://github.com/EdgeTX/edgetx/pull/5134))
* Precision setting for mix delay up & down (in addition to the precision for "slow up/down" that was added in 2.10) ([#5314](https://github.com/EdgeTX/edgetx/pull/5314))

### **Апаратури із кольоровим екраном**

* Radio user interface performance is significantly improved from that of 2.10 ([#5031](https://github.com/EdgeTX/edgetx/pull/5031))
* Top bar widget sizes can be changed ([#4846](https://github.com/EdgeTX/edgetx/pull/4846))
* File browser popup has filters to let you jump through the lists ([#4946](https://github.com/EdgeTX/edgetx/pull/4946))
* Full screen Lua widget "App mode", which gives widgets focus to allow for touch and key input ([#4655](https://github.com/EdgeTX/edgetx/pull/4655))
* Lua scripts and widgets can now use LVGL controls (buttons, sliders, input fields) - making it quicker and easier to make a _thing_ that interacts with the user ([#4887](https://github.com/EdgeTX/edgetx/pull/4887), [#5808](https://github.com/EdgeTX/edgetx/pull/5808))
* `PPM_US` can be used instead of percentage values ([#4987](https://github.com/EdgeTX/edgetx/pull/4987))
* Widgets can now have up to 10 options (was previously 5) ([#5365](https://github.com/EdgeTX/edgetx/pull/5365))

### Monochrome Screen Radios

* Collapsible sections in radio setup tab to make it shorter ([#5529](https://github.com/EdgeTX/edgetx/pull/5529))
* 'Set Screen' special function that lets you switch to a (configured) telemetry screen ([#5589](https://github.com/EdgeTX/edgetx/pull/5589))
* Displays PPM value in channel monitor (in addition to `0.0`/`0.00` value) ([#5781](https://github.com/EdgeTX/edgetx/pull/5781))
* Added option to invert display color ([#4933](https://github.com/EdgeTX/edgetx/pull/4933))
