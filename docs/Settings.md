# Settings

## Buffer size

Buffer size allows for setting the audio processing precision. A low buffer size corresponds to less precision and lower latency. A high buffer size corresponds to better precision and higher latency.  
A low buffer size is recommended when watching videos but not when listening to music.  
*On Android 9 it is recommended to max out buffer size, to minimize clipping issues in the lower frequencies*

## Legacy mode

Legacy mode is turned off by default, because features will become available in Wavelet whenever an application notifies your device system about music playback becoming active.  Some music players do not notify your device system, therefore no features will show up. You can try enabling legacy mode and see if your device allows Wavelet to process your music in this mode. Legacy might work, depending on your device manufacturer's audio framework implementation.  
You will have to experiment with legacy mode and see what works best.

:white_check_mark: List of players with support for audio processing:

* [YouTube Music](https://play.google.com/store/apps/details?id=com.google.android.apps.youtube.music)
* [Spotify Music](https://play.google.com/store/apps/details?id=com.spotify.music)
* [Jair Music Player](https://play.google.com/store/apps/details?id=aj.jair.music)
* [Phonograph Music Player](https://play.google.com/store/apps/details?id=com.kabouzeid.gramophone)
* [Shuttle Music Player](https://play.google.com/store/apps/details?id=another.music.player)
* [Samsung Music](https://play.google.com/store/apps/details?id=com.sec.android.app.music)
* [Google Play Music](https://play.google.com/store/apps/details?id=com.google.android.music)
* [Just (Video) Player](https://play.google.com/store/apps/details?id=com.brouken.player)
* [Podcast Addict](https://play.google.com/store/apps/details?id=com.bambuna.podcastaddict)
* [Poweramp](https://play.google.com/store/apps/details?id=com.maxmpz.audioplayer) (requires [additional configuration](/Configuration#poweramp))
* [Neutron](https://play.google.com/store/apps/details?id=com.neutroncode.mp) (requires [additional configuration](/Configuration#neutron))
* [Musicolet](https://play.google.com/store/apps/details?id=in.krosbits.musicolet) (requires [additional configuration](/Configuration#musicolet))
* [BlackPlayer](https://play.google.com/store/apps/details?id=com.musicplayer.blackplayerfree) (requires [additional configuration](/Configuration#blackplayer))
* [Deezer](https://play.google.com/store/apps/details?id=deezer.android.app) (requires [additional configuration](/Configuration#deezer))
* [VLC](https://play.google.com/store/apps/details?id=org.videolan.vlc) (requires [additional configuration](/Configuration#vlc))
* [Plexamp](https://play.google.com/store/apps/details?id=tv.plex.labs.plexamp) (requires [additional configuration](/Configuration#plexamp))

❌ List of players lacking support for audio processing:

* [Tidal](https://play.google.com/store/apps/details?id=com.aspiro.tidal) (issue filed)
* [SoundCloud](https://play.google.com/store/apps/details?id=com.soundcloud.android) ([issue filed](https://help.soundcloud.com/requests/483626/))
* [Music Player - MP3 Player, Audio Player](https://play.google.com/store/apps/details?id=musicplayer.musicapps.music.mp3player)
* [Amazon Music](https://play.google.com/store/apps/details?id=com.amazon.mp3)
* [Pulsar Music Player](https://play.google.com/store/apps/details?id=com.rhmsoft.pulsar)
* [Pocket Cast](https://play.google.com/store/apps/details?id=au.com.shiftyjelly.pocketcasts)
* [Stream YouTube Player](https://play.google.com/store/apps/details?id=com.djit.apps.stream)
* [YouTube](https://play.google.com/store/apps/details?id=com.google.android.youtube)
* [Pandora](https://play.google.com/store/apps/details?id=com.pandora.android)
* [Qobuz](https://play.google.com/store/apps/details?id=com.qobuz.music)
* [foobar2000](https://play.google.com/store/apps/details?id=com.foobar2000.foobar2000)
* Most music applications that came preinstalled on your device

## Enhanced session detection

**Disclaimer:** Enhanced session detection is experimental and available only for Android 10 and up.  
If you choose to activate enhanced session detection, Wavelet will actively listen for music sessions instead of relying on being notified when a session starts. The DUMP permission is required to allow Wavelet to filter the required information from the device system services needed to attach and release audio effects to audio sessions. The advantage of enhanced session detection is that there is no need to depend on other applications opening and closing their audio sessions properly, which means it should work properly with every media session.

Instructions to activate enhanced session detection:

- Activate developer options and enable USB debugging on your device as instructed on [developer.android.com/studio/debug/dev-options]
    - On Xiaomi devices, it is mandatory to enable 'USB debugging (Security Settings)' in developer options
    - On Realme and OPPO devices, it is mandatory to disable 'permission monitoring' under settings - security center
    - On OnePlus devices, it is mandatory to enable 'Disable permission monitoring' in developer options
- Connect your device with a computer
- Open Chrome on your computer, browse to [app.webadb.com/#/shell] and add and connect your device
- Run the following command in the shell: $ `pm grant com.pittvandewitt.wavelet android.permission.DUMP`
- Go to notification listener access and enable the permission for Wavelet

If you wish to switch back to the old behaviour, you can do so by disabling notification listener access for Wavelet and/or by running $ `pm  revoke com.pittvandewitt.wavelet android.permission.DUMP`.

[app.webadb.com/#/shell]: https://app.webadb.com/#/shell
[developer.android.com/studio/debug/dev-options]: https://developer.android.com/studio/debug/dev-options.html#enable