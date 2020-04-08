# RME-BabyFace-Pro-FS-Mixer-Patch

The Babyface Pro Fs features a DSP allowing to do quite a bit of routing. This patch exposes the different routing junctions to alsa mixer, hopefully motivating people to create a nice little GUI. ;)

Thanks RME for your support!

## Applying the patch
Patch with `patch --strip=1 < RME-Babyface-Pro-FS.patch` against your kernel sources.

Don't forget to activate the corresponding module in your config
`make M=sound/usb`

Feedback is always welcome and please use with caution! I've tested it quite a bit, but you'll never now. ;)

I might rename the volume controls before I get to submit this patch officially.
