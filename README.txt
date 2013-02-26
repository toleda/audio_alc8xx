audio_alc8xx
============
OS X Realtek ALC8xx Audio

This guide enables OS X Realtek ALC8xx onboard audio on Intel based motherboards with a bootable clean install of OS X.  Supported Realtek audio codecs are ALC885, ALC887, ALC888, ALC889, ALC892 and ALC898. The Optimized AppleHDA.kext only works with the codec the kext was edited for and replaces the native AppleHDA.kext. In Mountain Lion, the Optimized AppleHDA.kext supports 3 Audio_IDs:
Audio_ID: 1 supports 5 and 6 port ALC8xx onboard and/or AMD/Nvidia HDMI audio  
Audio_ID: 2 supports 3 port ALC8xx onboard and/or AMD/Nvidia HDMI audio
Audio_ID: 3 supports 3, 5 and 6 port ALC8xx onboard and HD3000/HD4000 HDMI audio

The are two techniques to enable the Optimized AppleHDA.kext:
1. no dsdt/audio enabler = Audio_ID
1a. Audio_ID = 1, HDAEnabler1.kext
1b. Audio_ID = 2, HDAEnabler2.kext
2. *dsdt/HDEF/layout-id = Audio_ID
2a. Audio_ID = 1, 0x01, 0x00, 0x00, 0x00, 0x00
2b. Audio_ID = 2, 0x02, 0x00, 0x00, 0x00, 0x00
2c. Audio_ID = 3, 0x03, 0x00, 0x00, 0x00, 0x00
*dsdt/HDEF/layout-id edits, see How_to_Add/Edit_dsdt/HDEF.pdf

More information, see Optimized_AppleHDA_for_ALC8xx.pdf

Installation - Optimized AppleHDA.kext http://www.tonymacx86.com/downloads.php?do=cat&id=3 MultiBest - Mountain Lion
1. no dsdt/audio enabler
1a. Audio_ID = 1, MultiBeast 5.2.1 or newer - Select/Drivers & Bootloaders/Drivers/Audio/Realtek ALC8xx/Without DSDT/ALC8--
1b. Audio_ID = 2, MultiBeast 5.2.1 or newer - Select/Drivers & Bootloaders/Drivers/Audio/Realtek ALC8xx/Without DSDT/ALC8--  and /Optional 3 Port Audio 
2. dsdt/HDEF/layout-id = 1, 2 or 3
2a. MultiBeast 5.2.1 or newer - Select/Drivers & Bootloaders/Drivers/Audio/Realtek ALC8xx/With DSDT/ALC8--

Troubleshooting
1. See Optimized_AppleHDA_for_ALC8xx.pdf 
2. Post to http://www.tonymacx86.com/audio/76309-mountain-lion-multibeast-no-audio-solutions-problem-reporting.html

toleda
https://github.com/toleda/audio_alc8xx
Patches
How_to_Add/Edit_dsdt/HDEF.pdf
Optimized_AppleHDA_for_ALC8xx.pdf
README.txt