# Settings

## Buffer size

Buffer size allows for setting the audio processing precision. A low buffer size corresponds to less precision and lower latency. A high buffer size corresponds to better precision and higher latency.  
A low buffer size is recommended when watching videos but not when listening to music.  
*On Android 9 it is recommended to max out buffer size, to minimize clipping issues in the lower frequencies*

## AIDL mode

AIDL mode is a workaround for the issues Google introduced with the new AIDL Audio HAL. Less features are available in this mode unfortunately. Enable this setting if Wavelet stopped working properly after a system update or if changing any setting in the equalization options has no effect. Currently known affected devices are the Pixel 9 series and Xiaomi 15. More devices are expected to suffer from these issues.

## Legacy mode

Legacy mode is turned off by default, because features will become available in Wavelet whenever an application notifies your device system about music playback becoming active.  Some music players do not notify your device system, therefore no features will show up. You can try enabling legacy mode and see if your device allows Wavelet to process your music in this mode. Legacy might work, depending on your device manufacturer's audio framework implementation.  
You will have to experiment with legacy mode and see what works best.

:white_check_mark: List of players with support for audio processing:

* [YouTube Music]
* [Spotify]
* [Plexamp]
* [Auxio]
* [Music Player GO]
* [Jair Music Player]
* [Phonograph Music Player]
* [Shuttle Music Player]
* [Samsung Music]
* [Just (Video) Player]
* [Podcast Addict]
* [Poweramp Music Player] (requires [additional configuration](Configuration.md#poweramp))
* [Neutron Music Player] (requires [additional configuration](Configuration.md#neutron))
* [Musicolet Music Player] (requires [additional configuration](Configuration.md#musicolet))
* [BlackPlayer Music Player] (requires [additional configuration](Configuration.md#blackplayer))
* [Deezer] (requires [additional configuration](Configuration.md#deezer))
* [VLC for Android] (requires [additional configuration](Configuration.md#vlc))

❌ List of players lacking support for audio processing:

* [TIDAL Music]
* [SoundCloud]
* [Apple Music] (Sometimes it does, but very buggy)
* [Music Player & MP3 Player]
* [Amazon Music]
* [Pulsar Music Player]
* [Pocket Casts]
* [YouTube]
* [Pandora]
* [Qobuz]
* [foobar2000]
* [LibreTube]
* Most music applications that came preinstalled on your device

## Enhanced session detection

**Disclaimer:** Enhanced session detection is experimental and available only for Android 10 and up.  
If you choose to activate enhanced session detection, Wavelet will actively listen for music sessions instead of relying on being notified when a session starts. The DUMP permission is required to allow Wavelet to filter the required information from the device system services needed to attach and release audio effects to audio sessions. The advantage of enhanced session detection is that there is no need to depend on other applications opening and closing their audio sessions properly, which means it should work properly with every media session.

Instructions to activate enhanced session detection:

1. Activate developer options and enable USB debugging on your device as instructed on [developer.android.com/studio/debug/dev-options]
    - On Xiaomi devices, it is mandatory to enable 'USB debugging (Security Settings)' in developer options
    - On Realme and OPPO devices, it is mandatory to disable 'permission monitoring' under settings - security center
    - On OnePlus devices, it is mandatory to enable 'Disable permission monitoring' in developer options
2. Grant DUMP permission
    1. Connect your device to any device with Chrome installed (or go to d.)
    2. Open Chrome on the host device, browse to [app.webadb.com/shell] and add and connect your device
    3. Run this command in the webadb shell:
    ```shell
    pm grant com.pittvandewitt.wavelet android.permission.DUMP
    ```
    4. Alternatively, if your device has a shell with ADB installed, run:
    ```shell
    adb shell pm grant com.pittvandewitt.wavelet android.permission.DUMP
    ```
3. Go to notification listener access and enable the permission for Wavelet

If you wish to switch back to the old behaviour, you can do so by disabling notification listener access for Wavelet and/or by running:
```shell
pm revoke com.pittvandewitt.wavelet android.permission.DUMP
```

[app.webadb.com/shell]: https://app.webadb.com/shell
[developer.android.com/studio/debug/dev-options]: https://developer.android.com/studio/debug/dev-options.html#enable

[Youtube Music]: https://play.google.com/store/apps/details?id=com.google.android.apps.youtube.music
[Spotify]: https://play.google.com/store/apps/details?id=com.spotify.music
[Plexamp]: https://play.google.com/store/apps/details?id=tv.plex.labs.plexamp
[Auxio]: https://f-droid.org/packages/org.oxycblt.auxio/
[Music Player GO]: https://play.google.com/store/apps/details?id=com.iven.musicplayergo
[Jair Music Player]: https://play.google.com/store/apps/details?id=aj.jair.music
[Phonograph Music Player]: https://play.google.com/store/apps/details?id=com.kabouzeid.gramophone
[Shuttle Music Player]: https://play.google.com/store/apps/details?id=another.music.player
[Samsung Music]: https://play.google.com/store/apps/details?id=com.sec.android.app.music
[Just (Video) Player]: https://play.google.com/store/apps/details?id=com.brouken.player
[Podcast Addict]: https://play.google.com/store/apps/details?id=com.bambuna.podcastaddict
[Poweramp Music Player]: https://play.google.com/store/apps/details?id=com.maxmpz.audioplayer
[Neutron Music Player]: https://play.google.com/store/apps/details?id=com.neutroncode.mp
[Musicolet Music Player]: https://play.google.com/store/apps/details?id=in.krosbits.musicolet
[BlackPlayer Music Player]: https://play.google.com/store/apps/details?id=com.musicplayer.blackplayerfree
[Deezer]: https://play.google.com/store/apps/details?id=deezer.android.app
[VLC for Android]: https://play.google.com/store/apps/details?id=org.videolan.vlc

[TIDAL Music]: https://play.google.com/store/apps/details?id=com.aspiro.tidal
[SoundCloud]: https://play.google.com/store/apps/details?id=com.soundcloud.android
[Apple Music]: https://play.google.com/store/apps/details?id=com.apple.android.music
[Music Player & MP3 Player]: https://play.google.com/store/apps/details?id=musicplayer.musicapps.music.mp3player
[Amazon Music]: https://play.google.com/store/apps/details?id=com.amazon.mp3
[Pulsar Music Player]: https://play.google.com/store/apps/details?id=com.rhmsoft.pulsar
[Pocket Casts]: https://play.google.com/store/apps/details?id=au.com.shiftyjelly.pocketcasts
[YouTube]: https://play.google.com/store/apps/details?id=com.google.android.youtube
[Pandora]: https://play.google.com/store/apps/details?id=com.pandora.android
[Qobuz]: https://play.google.com/store/apps/details?id=com.qobuz.music
[foobar2000]: https://play.google.com/store/apps/details?id=com.foobar2000.foobar2000
[LibreTube]: https://f-droid.org/packages/com.github.libretube/