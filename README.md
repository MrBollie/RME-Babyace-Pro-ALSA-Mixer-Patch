# RME Babyface Pro Patch for ALSA Mixer

The Babyface Pro and its FS-successor feature a DSP allowing to do quite a bit of routing. This patch exposes the different routing junctions to alsa mixer, hopefully motivating people to create a nice little GUI. ;)

Thanks RME for your support!

## Applying the patch
Patch with `patch --strip=1 < RME-Babyace-Pro-ALSA-Mixer.patch` against your kernel sources.

Don't forget to activate the corresponding module in your config
`make M=sound/usb`

Feedback is always welcome and please use with caution! I've tested it quite a bit, but you'll never now. ;)

I might rename the volume controls before I get to submit this patch officially.

## Using a Mixer GUI

Exposing so many controls will cause inconvenience when using standard mixer apps like alsamixer. Therefore, a custom mixer GUI is probably the best way to go. I'm currently working on a very basic one, you will find here: https://github.com/MrBollie/bbfpromix 

Of course, feel free to code your own, probably way more sophisticated one. :)

___

[![ko-fi](https://www.ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/I2I61NTVW)
