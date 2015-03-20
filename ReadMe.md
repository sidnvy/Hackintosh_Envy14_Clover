---
### 1. DSDT Patch

Get **DSDT.dsl** and **SSDT-x.dsl** using command  
`$ iasl -dl -da *.aml`

And patch **.dsl** file using maciASL 

* **DSDT.dsl**
	1. Fix PARSEOP_STORE ...
	2. Rename GFX0 -> IGPU
	3. Battery patch
	4. Fn bright key patch
	6. AC Adapter Fix
	7. Haswell LPC patch 
* **SSDT-4.dsl**
	1. Rename GFX0 -> IGPU
	2. Brightness fix (Haswell)
* **SSDT-5.dsl**
	1. Rename GFX0 -> IGPU
	2. Disable from _INI(the NVidia)

Save all ***.dsl** file as **AML** and put them to /EFI/CLOVER/ACPI/patched

---
### 2. Kext to install 

*  ACPIBacklight.kext
2. ACPIBatteryManager.kext
3. AppleHDADisabler.kext
4. FakePCIID_HD4600_HD4400.kext
5. FakePCIID.kext
6. FakeSMC.kext
7. RealtekRTL8111.kext
8. VoodooHDA.kext
9. VoodooPS2Controller.kext

Kext and Tools can find [Here on Google Drive ](https://drive.google.com/folderview?id=0B4zR-e_IblY1flpoY3daeG9CVXBPSEZGM1lUOHBvMHA0cHlJaVQtWG5WUHRlckFvUmZzTEE&usp=sharing)