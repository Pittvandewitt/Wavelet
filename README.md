## Wavelet readme

### Compatible mode
Compatible mode is turned on by default. Whenever a compatible music application starts a session while Wavelet is running, features will become available. If nothing is showing up, you can try toggling the compatible mode checkbox and see if your music player works in legacy mode. You will have to experiment with this to see what works best.
A few apps that work with compatible mode are Spotify, YT music, Shuttle, Phonograph and Google Play Music.
Tidal, YouTube, Soundcloud, Qobuz, Neutron, PowerAmp and most music apps that came preinstalled with your phone may work in legacy mode, depending on your phone manufacturer's implementation

### AutoEq
The [AutoEq](https://github.com/jaakkopasanen/AutoEq) feature contains precalculated results from jaakkopasanen's great work. Over 2000 entries are shipped with Wavelet and contain the optimal compensation in frequency response for those specific headphones
- __Headphone model__ lets you search the database or view your previously selected headphones. Tap the search icon next to the title to add new listings or tap the x icon to remove an item if you selected the wrong one. Make sure to only use the entry that is meant for your headphone model

### Graphic equalizer
The graphic equalizer consists of 9 bands. You can set each slider independently to change the balance in frequency response. You can use this to remove most obivous imbalance If you use speakers or your headphone is not listed, you can use this feature to compensate. You can also add coloration you prefer listening to
- __Presets__ contains a few presets for a given set of music genres. The first entry will reset all bands to stock

### Bass boost
Bass boost amplifies the lower frequencies
- __Bass boost strength__ lets you set the strength in decibel

### Reverberation
Reverberation adds the effect of a sound bouncing of the wall from a room you would be listening in
- __Preset__ lets you choose the room size

### Virtualizer
Virtualization is the effect of spatializing audio channels. When listening in stereo, this effect will widen the stereo image. 
- __Strength__ determines the effect strenght

### Limiter
The limiter removes volume spikes from your audio. Sometimes this is desired in noisy environments where you need to turn up the volume in quite parts of the music and later turn it down when the music becomes louder  
- __Attack time__ determines after how many milliseconds the effect will kick in. A fast time will help remove unwanted peaks very effectively, but is very noticable. A longer attack time might not be fast enough, but it will sound more natural
- __Release time__ determines how long the effect will be active. A fast time will give that pumping sound. A long time will sound smoother but may negate a fast attack time and affect transients in your music
- __Ratio__ sets the effect strength. If a signal is 1dB over the threshold, it will reduce the output by the ratio level you set
- __Threshold__ determines above what volume level the limiter should become effective

### Channel balance
Channel balance allows you to control the left and right channel output volume separately. This can come in handy when you can't sit in center of your speaker setup or when your headphones have a difference in impedance between your left and right channel  
Some phones have a limiter built in that causes volume ducking when you boost above a certain amount of dB. You can use this feature to control the overall volume output and to prevent this ducking from happening
- __Channel gain__ controls the balance between left and right