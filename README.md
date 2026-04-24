# This is only useful for switch with corrupted SYSTEM partition

* I'm not responsible of any mistake you'll make
* It will fix sysmodule related error like error **2002-0038** with program id **0100000000000039** or **010000000000003E**

# Tools needed

* [Tegraexplorer](https://github.com/suchmememanyskill/TegraExplorer) : to launch the script
* [NxNandManager](https://github.com/eliboa/NxNandManager) : to mount partition file
* [EmmcHaccGen](https://github.com/suchmememanyskill/EmmcHaccGen) : to create a valid SYSTEM partition
* The corresponding firmware the broken eMMC is on (use Hekate InfoTools or FuseCheck to find the correct one)

  * It needs to be the matching one to prevent bootloop and other errors
  * Other version can be tested at your own risks
* Minimal CFW Switch with Hekate (No need of a fully functioning sys/emummc, just Hekate access)
* Switch with at least a working PRODINFO to get bis keys to sign system saves

# Better backup eMMC RAW GPP

* **Backup your eMMC even if it's corrupt/non working**
* If you're here, it's highly likely that **you don't have a valid backup**
* Don't worry, maybe it will work. It worked for me with a very corrupt SYSTEM partition

# Steps

1. Copy **CorruptSystemNandFixer.te** to your sdcard
2. Run it using tegraexplorer
3. Choose option 1 to backup your SYSTEM partition to sdcard:/RestoreSystem/SYSTEM.bin

   * Make sure you have at least ~2.5Gb of free space on your sdcard
4. Select SYSTEM.bin using NxNandManager
5. Wipe the partition using NxNandManager (there is a button to do so after selecting the partition)
6. Run EmmcHaccGen and generate SYSTEM folder

   * Use [suchmememanyskill unbrick guide](https://suchmememanyskill.github.io/guides/unbrick/) to create it
7. Copy the contents of the generated SYSTEM folder to the mounted recently wiped SYSTEM partition
8. Rerun the script from tegraexplorer and choose option 2

   * It will automatically sign saves
9. Do a system wipe (eMMC or emuMMC depending on what you fixed)

   * Look for the correct section about that in [suchmememanyskill unbrick guide](https://suchmememanyskill.github.io/guides/unbrick/)
10. Reboot corresponding eMMC (eMMC or emuMMC depending on what you fixed)
