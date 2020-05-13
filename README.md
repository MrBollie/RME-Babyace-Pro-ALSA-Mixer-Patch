# RME Babyface Pro Patch for ALSA Mixer

The Babyface Pro and its FS-successor feature a DSP allowing to do quite a bit of routing. This patch exposes the different routing junctions to alsa mixer, hopefully motivating people to create a nice little GUI. ;)

Thanks RME for your support!

## Applying the patch
This patch has been [merged to upstream Linux](https://git.kernel.org/pub/scm/linux/kernel/git/tiwai/sound.git/commit/?h=for-next&id=3e8f3bd047163d30fb1ad32ca7e4628921555c09) for Linux 5.8. If your distribution does not yet package Linux 5.8, you can apply this patch to your distribution's kernel sources. Consult your distribution's documentation details about how to build your own kernel.

Patch with `patch --strip=1 < RME-Babyace-Pro-ALSA-Mixer.patch` against your kernel sources.

Don't forget to activate the corresponding module in your config
`make M=sound/usb`

Feedback is always welcome and please use with caution! I've tested it quite a bit, but you'll never now. ;)

## Using a Mixer GUI

Exposing so many controls will cause inconvenience when using standard mixer apps like alsamixer. Therefore, a custom mixer GUI is probably the best way to go. I'm currently working on a very basic one, you will find here: https://github.com/MrBollie/bbfpromix 

Of course, feel free to code your own, probably way more sophisticated one. :)

___

[![ko-fi](https://www.ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/I2I61NTVW)
