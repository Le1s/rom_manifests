# LeEco Le 1s (x3) Device trees

Hello everyone, this repo contains a few variations of device tree to build different custom ROMs.

# About Device

![LeEco Le1S](http://cdn2.gsmarena.com/vv/pics/leeco/letv-le-1s-1.jpg "LeEco Le1S")

## Specifications

Basic   | Spec Sheet
-------:|:-------------------------
CPU     | Octa-core 2.2 GHz Cortex-A53
Chipset | Mediatek MT6795 Helio X10
GPU     | PowerVR G6200
Memory  | 3GB
Storage | 32GB
Battery | Non-removable Li-Po 3000 mAh battery
Display | 1080 x 1920 pixels (~401 ppi pixel density) 5.5 inches
Camera  | Primary: 13 MP, Secondary: 5 MP

---

# Branches
Currently, this repo have branches for device trees for following ROMs:

No.| ROM            | ROM Version |Android Version | Branch    | Local Branch | Manifest Name
--:|:---------------|:------------|:---------------|:----------|:-------------|:-------------
1  | LineageOS      | 14.1        | 7.1.2          | cm-14.1   | cm-14.1      | x3_lineage_nougat.xml
2  | Dirty Unicorns | 11.5        | 7.1.2          | n7x       | n7x          | x3_du_nougat.xml
3  | AOSPA          | 7.1.3       | 7.1.2          | mougat-mr2| nougat-pa    | x3_AOSPA_nougat.xml
3  | Carbon         | 5.1         | 7.1.2          | cr-5.1    | cr-5.1       | x3_carbon_nougat.xml
4  | LineageOS      | 13.0        | 6.0.1          | cm-13.0   | cm-13.0      | x3_lineage_mm.xml


More might come.

---

# How to build.
Unless you know what you are doing, You'd need to follow these simple steps in order to build any of the supported using this tree.

## Steps:
* init the repo of whichever rom you want to build.
* wget that ROM's manifest in the ".repo/local_manifests"(might need to mkdir first) of your work directory from this repo, like:
  "$ cd .repo/local_manifests
   $ wget https://github.com/SscSPs/android_device_leeco_x3/raw/master/x3_lineage_nougat.xml "
  for LineageOS 14.1
* Do the "repo sync" to get files

That's it.
Now you can proceed to build the rom in normal way.
for that, just follow these simple commands in the terminal,
from root of your source(the place where you did the repo init):
* . build/envsetup.sh
* breakfast x3
* make bacon -j8

This will build the rom and the generated zip will be in out/target/product/x3 directory.

---

## THANKS TO:
I would like to Thank the following people, they have helped in making one or more of these
trees in one way or the other. All this would not have been possible without them.

* WisniaPL
* DeckerSU
* M.A.D
* Bule
* Danielhk
* PokeTrainerRed

---

If you have any question(s) open an issue, or contact me on telegram @FearTheBatman

---
