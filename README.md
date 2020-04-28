# SteelSeries Arctis 5 for Linux

 
The SteelSeries Arctis 5 is a gaming headset, which has two stereo audio outputs. One for voice chat and one for the rest of the sound. It can be mixed between with a physical knob.


## Pulseaudio Profile

By default, pulseaudio only enables the voice chat output (testing on Ubuntu Bionic). This profile enables the second (game) output and the udev rule makes sure this profile is used when plugging in the device.


### Installing


#### Ubuntu / Linux Mint

See instructions on http://www.arakhne.org/unbuntu.html and install the package `pulseaudio-stellseries-arctis-5`.

#### From Source

Install from by copying the following files:

* `91-pulseaudio-steelseries-arctis-5-game-channel.rules` to `/lib/udev/rules.d/`


The following files are already well-configured on Ubuntu Bionic:

* `/usr/share/pulseaudio/alsa-mixer/paths/steelseries-arctis-5-output-game.conf`
* `/usr/share/pulseaudio/alsa-mixer/paths/steelseries-arctis-5-output-chat.conf`
* `/usr/share/pulseaudio/alsa-mixer/profile-sets/steelseries-arctis-5-usb-audio.conf`


Restart Pulseaudio:

	pulseaudio -k
	pulseaudio --start


After that, plug in the device to see if it works.

