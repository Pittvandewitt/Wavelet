#  Wavelet

## [Troubleshooting](https://pittvandewitt.github.io/Wavelet/Troubleshooting)

## Legacy mode

Legacy mode is turned off by default, because features will become available in Wavelet whenever an application notifies the operating system about music playback starting by sending a broadcast.  
Spotify, YT music, Shuttle, Phonograph, Google Play Music and many more music players send a broadcast, thus features in Wavelet will show up.  
Some players like Poweramp, Neutron, Musicolet, BlackPlayer and Deezer require [additional configuration](https://pittvandewitt.github.io/Wavelet/Configuration).  
Tidal, Pandora, YouTube, Soundcloud, Qobuz, VLC, Plexamp, foobar2000 and most music applications that came preinstalled on your phone, do not send a broadcast. Therefore no features will show up. You can try enabling legacy mode and see if your device allows Wavelet to process your music in this mode. Legacy might work, depending on your device manufacturer's audio framework implementation.  
You will have to experiment with legacy mode and see what works best.

## Reduce clipping

By enabling clipping reduction, you allow Wavelet to process audio in a bigger time frame (170 vs 22ms) This reduces clipping at cost of increased latency. Recommended when listening to music but not when watching videos.

## AutoEq

The [AutoEq](https://github.com/jaakkopasanen/AutoEq) feature contains precalculated results from jaakkopasanen's great work. Over 2500 entries are shipped with Wavelet and contain the optimal frequency response compensation for those specific headphone models.

- __Headphone model__ lets you search the database or view your previously selected headphones. Tap the search icon next to the title to add new listings or tap the x icon to remove an item if you selected the wrong one. *Make sure to only use the entry that is meant for your headphone model*.

- __Import__ Allows you to load custom generated AutoEq data. Instructions can be found [here](https://pittvandewitt.github.io/Wavelet/Import).

## Graphic equalizer

The graphic equalizer consists of 9 bands. You can set each slider independently to change the balance in frequency response or to remove obvious imbalance issues. You can also use this feature to compensate the frequency response of your speakers or your headphones if they're are not listed in the AutoEq section, or if you would like to add some coloration to your audio stream.

- __Presets__ contains a few presets for a given set of sound signatures. The first entry will reset all bands to stock.

## Bass boost

Bass boost amplifies the lower frequencies.

- __Bass boost strength__ lets you set the strength.

## Reverberation

Reverberation adds the effect of a sound bouncing of the wall from a room you would be listening in.

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
