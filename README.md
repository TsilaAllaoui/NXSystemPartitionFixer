# This is only useful for switch with corrupted SYSTEM partition
- I'm not responsible of any mistake you'll make
- It will fix sysmodule related error like error **2002-0038** with program id **0100000000000039** or **010000000000003E**

# Tools needed
- [Tegraexplorer](https://github.com/suchmememanyskill/TegraExplorer) : to launch the script
- Minimal CFW Switch with Hekate (No need of a fully functioning sys/emummc, just Hekate access)
- Switch with at least a working PRODINFO to get keys

# Better backup eMMC RAW GPP
- If you're here, it's highly likely that you don't have a valid backup
- Don't worry, maybe it will work. It worked for me with a very corrupt SYSTEM partition

# This will copy SYSTEM folder in "sd:/RestoreSystem/SYSTEM" to SYSTEM partition
- The source SYSTEM folder should be generated using [EmmcHaccGen](https://github.com/suchmememanyskill/EmmcHaccGen) and should be placed in sdcardroot:/RestoreSystem folder
  - Specific console's BIS keys will be needed to generate this
- The target SYSTEM partition should be the switch's sysMMC SYSTEM partition mounted via [Hekate](https://github.com/CTCaer/hekate) or an emuMMC SYSTEM partition mounted with [NxNandManager](https://github.com/eliboa/NxNandManager)

# Useful links
- [suchmememanyskill unbrick guide](https://suchmememanyskill.github.io/guides/unbrick/)