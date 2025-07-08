# Troubleshooting

## In-app purchase no longer available
The in-app purchase is a one time only purchase without expiry. It is saved to your Google account. Therefore, confirm you are logged in with the Google account you made the purchase with. In case your purchase is not detected by Wavelet, you are adviced to vist the Wavelet listing in the Play Store on the device where the purchase is not detected. Opening Wavelet through Google Play will restore the purchase.  
[Open Wavelet :fontawesome-brands-google-play:](https://play.google.com/store/apps/details?id=com.pittvandewitt.wavelet){ .md-button }  


## Headphone model not listed in AutoEq
All data included in Wavelet comes from the AutoEq project which takes its data from external sources. If none of the sources have measured a particular headphone model, the model cannot be included in AutoEq.  
If you were able to find a frequency response measurement of your headphones, you can try to create compensation data by following the [import instructions].


## Wavelet randomly stopping
Many OEMs apply nasty battery saving techniques, such as limiting applications to start automatically or killing applications even when the application is in use. It is highly recommendend to check out [dontkillmyapp.com] and follow the instructions for your device brand to prevent issues like these from happening.


## Legacy mode does not work via Bluetooth
Go to your device [developer options] and turn off "Disable Bluetooth A2DP hardware offload".


## No sound difference via Bluetooth device or external DAC
Some devices ship libraries used by Wavelet that don't support the sample rate used by your Bluetooth device or DAC. To fix this issue for Bluetooth devices, go to your device [device developer] options and set the Bluetooth sample rate to 48kHz and/or the Bluetooth codec to SBC.  
Unfortunately no solution is known for external DACs.


## Clipping issues on Samsung devices
Some Samsung devices have a UHQ upscaler in the 'Sound quality and effects' system settings. Change the UHQ upscaler to Bit upscaling only to avoid clipping issues.


## Other
Wavelet will often not function as expected if other equalizer/hearing aid applications are installed, such as:
- Sound assistant on some Samsung devices
- AudioFX on LineageOS
- 3rd party equalizer applications installed from the Play Store

Freezing or uninstalling the offending application + rebooting your device will resolve issues caused by this.

[import instructions]: Import.md
[developer options]: https://developer.android.com/studio/debug/dev-options.html#enable
[dontkillmyapp.com]: https://dontkillmyapp.com/