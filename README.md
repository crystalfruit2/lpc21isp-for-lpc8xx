# lpc21isp-for-lpc8xx
lpc21isp patched lpcprog.c file for lpc8xx version of the microcontrollers.

Mac flashmagic alternative download

1) You can just download the repository files

2) Or follow trough the steps down below
Lpc21isp is a “command line program” that lets you program the microcontroller using the terminal of mac and linux, Use the sourceforge link to download it https://sourceforge.net/projects/lpc21isp/


Version 1.97 doesn’t support it so we need to change the “lpcprog.c” file to use it. You can use “Nano” or “Vim” editor to change the file inside the terminal easily 
Don’t use homebrew to download the lpc21isp this makes it harder to change the files from the bin folder.
```

static LPC_DEVICE_TYPE LPCtypes[] =
{
{ 0, 0, 0, 0, 0, 0, 0, 0, 0, CHIP_VARIANT_NONE }, /* unknown */
// id, id2, use id2, name of product, flash size, ram size, total number of sector, max copy size, sector table, chip variant
{ 0x00008100, 0x00000000, 0, "810M021FN8", 4, 1, 4, 256, SectorTable_8xx, CHIP_VARIANT_LPC8XX },
{ 0x00008110, 0x00000000, 0, "811M001FDH16", 8, 2, 8, 1024, SectorTable_8xx, CHIP_VARIANT_LPC8XX },
{ 0x00008120, 0x00000000, 0, "812M101FDH16", 16, 4, 16, 1024, SectorTable_8xx, CHIP_VARIANT_LPC8XX },
{ 0x00008121, 0x00000000, 0, "812M101FD20", 16, 4, 16, 1024, SectorTable_8xx, CHIP_VARIANT_LPC8XX },
{ 0x00008122, 0x00000000, 0, "812M101FDH20", 16, 4, 16, 1024, SectorTable_8xx, CHIP_VARIANT_LPC8XX },
{ 0x00008241, 0x00000000, 0, "LPC824M201", 32, 8, 32, 1024, SectorTable_8xx, CHIP_VARIANT_LPC8XX },
{ 0x00008242, 0x00000000, 0, "824M201JDH20", 32, 8, 32, 1024, SectorTable_8xx, CHIP_VARIANT_LPC8XX },



```
Save, make and run.

IMPORTANT: not sure about the 25th line check with and without if not working correctly 




