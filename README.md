# RME Babyface Pro Patch for ALSA Mixer

**Important:** Project will be archived soon, as the code has been part of the mainline kernel since 2020 and I'm no longer maintaining it

The Babyface Pro and its FS-successor feature a DSP allowing to do quite a bit of routing. This patch exposes the different routing junctions to alsa mixer, hopefully motivating people to create a nice little GUI. ;)

Thanks RME for your support!

## Applying the patch

**As this has been part of the mainline kernel since 2020, this shouldn't been needed anymore.**

Patch with `patch --strip=1 < RME-Babyace-Pro-ALSA-Mixer.patch` against your kernel sources.

Don't forget to activate the corresponding module in your config
`make M=sound/usb`

Feedback is always welcome and please use with caution! I've tested it quite a bit, but you'll never now. ;)

I might rename the volume controls before I get to submit this patch officially.

## Using a Mixer GUI

Exposing so many controls will cause inconvenience when using standard mixer apps like alsamixer. Therefore, a custom mixer GUI is probably the best way to go. I'm currently working on a very basic one, you will find here: https://github.com/MrBollie/bbfpromix 

Of course, feel free to code your own, probably way more sophisticated one. :)

## What this patch offers

- Access to the BBF Pro's internal mixer DSP to set level of individual routing crosspoints via alsa mixer
- Access to control registers to set SPDIF and clock master flags.

## What this patch doesn't offer

- Reading the current status from the device
- Exposing any level meters
- Access to EQ
- Access to preamp gain
- FX (those aren't really part of the DSP anyway)

The reason for these missing features is, that I wasn't provided with any USB control endpoint requests that would allow access to that. Please refrain from asking about features TotalMix on the iPad offers, that aren't available here, since it's done in a completely different way, that wouldn't belong into alsa mixer anyway.

