# Troubleshooting

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

## ChromeOS
It is not possible to detect a connected headphone in the Android subsystem on ChromeOS. Fortunately it is possible to mimick a headphone connection using [LesserAudioSwitch](https://play.google.com/store/apps/details?id=com.nordskog.LesserAudioSwitch). The app states it does not work on Android 11 and up, but a different solution is provided in the description.


## Other
Wavelet will often not function as expected if other equalizer/hearing aid applications are installed, such as:
- Sound assistant on some Samsung devices
- AudioFX on LineageOS
- 3rd party equalizer applications installed from the Play Store

Freezing or uninstalling the offending application + rebooting your device will resolve issues caused by this.

[Navigate to homepage](https://pittvandewitt.github.io/Wavelet/)