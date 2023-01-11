# Troubleshooting

## In-app purchase no longer available
The in-app purchase is for one time only and will stay valid. In case your purchase is not detected by Wavelet, you are adviced to clear Play Store data by going to your system settings - apps. Your purchase will reload and be made available to Wavelet again after you reboot your device.


## Headphone model not listed in AutoEq
All data included in Wavelet comes from the AutoEq project which takes its data from external sources. If none of the sources have measured a particular headphone model, the model cannot be included in AutoEq.  
If you were able to find a frequency response measurement of your headphones, you can try to create compensation data by following the instructions provided [here](https://pittvandewitt.github.io/Wavelet/Import).


## Wavelet service stopping / no longer applying effects when music playback has started
Many OEMs apply nasty battery saving techniques, such as limiting applications to start automatically or killing applications even when the application is in use. It is highly recommendend to check out [dontkillmyapp.com](https://dontkillmyapp.com/) and follow the instructions for your device brand to prevent issues like these from happening.


## No sound difference when listening through a Bluetooth device or external DAC
Some devices ship libraries used by Wavelet that don't support the sample rate used by your Bluetooth device or DAC. To fix this issue for Bluetooth devices, go to your device developer options and set the Bluetooth sample rate to 48kHz and/or the Bluetooth codec to SBC.  
If you can't find the developer options, search for build number in your system settings and tap it 5 times to enable developer options.  
Unfortunately no solution is known for external DACs.


## Clipping issues on your Samsung device
Some Samsung devices have a UHQ upscaler in the 'Sound quality and effects' system settings. Change the UHQ upscaler to Bit upscaling only to avoid clipping issues.

## Crackling/clipping issues on your Google Pixel device
AutoEq seems to cause audible crackling or clipping on some Google Pixel devices.

To resolve, try the following until the crackling goes away:

- Ensure buffer size is set to the maximum. Tap the cog at the bottom left of Wavelet's main screen. Then, drag the Buffer size slider to the end.
- Turn on the Limiter built-in to Wavelet. Then, tap Limiter and set the Post-gain to between -4.5db and -5.0db.
- Lower the AutoEQ strength. Tap AutoEq, then tap the EQ graph and set the strength to a value below 100%, until the crackling is no longer audible.

If none of the above helps, comment on or follow [the ongoing issue on GitHub](https://github.com/Pittvandewitt/Wavelet/issues/46).


## Other
Wavelet will often not function as expected if other equalizer/hearing aid applications are installed, such as:
- Sound assistant on some Samsung devices
- AudioFX on LineageOS
- 3rd party equalizer applications installed from the Play Store

Freezing or uninstalling the offending application + rebooting your device will resolve issues caused by this.

[Navigate to homepage](https://pittvandewitt.github.io/Wavelet/)
