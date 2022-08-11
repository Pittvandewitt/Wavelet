#  Wavelet

## [Troubleshooting](https://pittvandewitt.github.io/Wavelet/Troubleshooting)

## Legacy mode

Legacy mode is turned off by default, because features will become available in Wavelet whenever an application notifies the operating system about music playback starting by sending a broadcast.  Many music players send a broadcast, thus features in Wavelet will show up.  Other music players do not send a broadcast. Therefore no features will show up. You can try enabling legacy mode and see if your device allows Wavelet to process your music in this mode. Legacy might work, depending on your device manufacturer's audio framework implementation.  
You will have to experiment with legacy mode and see what works best.

:heavy_check_mark: List of players with support for audio processing:
* [YouTube Music](https://play.google.com/store/apps/details?id=com.google.android.apps.youtube.music)
* [Spotify Music](https://play.google.com/store/apps/details?id=com.spotify.music)
* [Auxio](https://f-droid.org/en/packages/org.oxycblt.auxio/)
* [Jair Music Player](https://play.google.com/store/apps/details?id=aj.jair.music)
* [Phonograph Music Player](https://play.google.com/store/apps/details?id=com.kabouzeid.gramophone)
* [Shuttle Music Player](https://play.google.com/store/apps/details?id=another.music.player)
* [Samsung Music](https://play.google.com/store/apps/details?id=com.sec.android.app.music)
* [Google Play Music](https://play.google.com/store/apps/details?id=com.google.android.music)
* [Just (Video) Player](https://play.google.com/store/apps/details?id=com.brouken.player)
* [Podcast Addict](https://play.google.com/store/apps/details?id=com.bambuna.podcastaddict)
* [Poweramp](https://play.google.com/store/apps/details?id=com.maxmpz.audioplayer) (requires [additional configuration](https://pittvandewitt.github.io/Wavelet/Configuration#poweramp))
* [Neutron](https://play.google.com/store/apps/details?id=com.neutroncode.mp) (requires [additional configuration](https://pittvandewitt.github.io/Wavelet/Configuration#neutron))
* [Musicolet](https://play.google.com/store/apps/details?id=in.krosbits.musicolet) (requires [additional configuration](https://pittvandewitt.github.io/Wavelet/Configuration#musicolet))
* [BlackPlayer](https://play.google.com/store/apps/details?id=com.musicplayer.blackplayerfree) (requires [additional configuration](https://pittvandewitt.github.io/Wavelet/Configuration#blackplayer))
* [Deezer](https://play.google.com/store/apps/details?id=deezer.android.app) (requires [additional configuration](https://pittvandewitt.github.io/Wavelet/Configuration#deezer))
* [VLC](https://play.google.com/store/apps/details?id=org.videolan.vlc) (requires [additional configuration](https://pittvandewitt.github.io/Wavelet/Configuration#vlc))
* [Plexamp](https://play.google.com/store/apps/details?id=tv.plex.labs.plexamp) (requires [additional configuration](https://pittvandewitt.github.io/Wavelet/Configuration#plexamp))

:x: List of players lacking support for audio processing:
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

- Activate developer options and enable USB debugging on your device as instructed on [https://developer.android.com/studio/debug/dev-options](https://developer.android.com/studio/debug/dev-options.html#enable)
  - On Xiaomi devices, it is mandatory to enable USB debugging (Security Settings)
  - On Realme and OPPO devices, it is mandatory to disable permission monitoring under settings - security center
- Connect your device with a computer
- Open Chrome on your computer, browse to [https://app.webadb.com/#/shell](https://app.webadb.com/#/shell)
and add and connect your device
- Run the following command in the shell: `pm grant com.pittvandewitt.wavelet android.permission.DUMP`
- Go to notification listener access and enable the permission for Wavelet

If you wish to switch back to the old behaviour, you can do so by disabling notification listener access for Wavelet and/or by running `pm revoke com.pittvandewitt.wavelet android.permission.DUMP`.

## Buffer size

Buffer size allows for setting the audio processing precision. A low buffer size corresponds to less precision and lower latency. A high buffer size corresponds to better precision and higher latency.  
A low buffer size is recommended when watching videos but not when listening to music.  
*On Android 9 it is recommended to max out buffer size, to minimize clipping issues in the lower frequencies*

## AutoEq

The [AutoEq](https://github.com/jaakkopasanen/AutoEq) feature contains precalculated results from jaakkopasanen's great work. Over 2500 entries are shipped with Wavelet and contain the optimal frequency response compensation for those specific headphone models.

- __Headphone model__ lets you search the database or view your previously selected headphones. Tap the search icon next to the title to add new listings or tap the x icon to remove an item if you selected the wrong one. *Make sure to only use the entry that is meant for your headphone model*.

- __Import__ Allows you to load custom generated AutoEq data. Instructions can be found [here](https://pittvandewitt.github.io/Wavelet/Import).

## Graphic equalizer

The graphic equalizer consists of 9 bands. You can set each slider independently to change the balance in frequency response or to remove obvious imbalance issues. You can also use this feature to compensate the frequency response of your speakers or your headphones if they're are not listed in the AutoEq section, or if you would like to add some coloration to your audio stream.

- __Presets__ contains a few presets for a given set of sound signatures. The first entry will reset all bands to stock.

## Bass boost

Bass boost is available on Android 9 exclusively. It amplifies the lower frequencies.

- __Bass boost strength__ lets you set the strength.

## Reverberation

Reverberation is available if legacy mode is disabled. It adds the effect of a sound bouncing of the wall from a room you would be listening in.

- __Preset__ lets you choose the room size.

## Virtualizer

Virtualization is the effect of spatializing audio channels. This effect will widen the stereo image (when listening in stereo).

- __Strength__ determines the effect strength.

## Bass tuner

Bass tuner allows you to set a very precise bass boost or reduction. This can be useful if your speaker system has a resonant peak in the lower frequencies or a point where long soundwaves cancel each other out.

- __Bass type__ Allows you to choose between natural, transient compressor and sustain compressor types. The transient compressor adds the possibility to increase or decrease the initial bass punch. The sustain compressor preserves the transient and is able to increase or reduce the rumble. This can be used to reduce resonance without compromising the initial kick or to make balanced armature drivers sound less anemic.

- __Cutoff frequency__ determines until what frequency the sound is processed.

- __Post-gain__ sets the gain to compensate for. This value can either be negative or positive.

## Limiter

The limiter removes volume spikes from your audio streams. Sometimes this is desired in noisy environments where you need to turn up the volume in quiet parts of the music and later turn it down when the music becomes louder.

- __Attack time__ determines after how many milliseconds the effect will kick in. A fast time will help remove unwanted peaks very effectively, but is very noticable. A longer attack time might not be fast enough, but it will sound more natural.

- __Release time__ determines how long the effect will be active. A fast time will give that pumping sound. A long time will sound smoother, but may negate a fast attack time and affect transients in your music.

- __Ratio__ sets the effect strength. If a signal is 1dB over the threshold, it will reduce the output by the ratio level you set.

- __Threshold__ determines above what volume level the limiter should become effective.

- __Post-gain__ allows you to compensate for volume changes caused ratio and threshold.

## Channel balance

Channel balance allows you to control the left and right channel output volumes separately. This can come in handy when you can't sit in center of your speaker setup or when your headphones have a difference in impedance between their left and right channels.
Some phones have a limiter built in that causes volume ducking when you boost above a certain amount of dB. You can also use this feature to control the overall volume output and to prevent this ducking from happening.

- __Channel gain__ controls the balance between left and right.
