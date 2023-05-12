---
layout: default
title: Home
nav_order: 1
description: A quick rundown on each feature and its settings
permalink: /
---

<script>
  switch(document.location.hash) {
    case "#legacy-mode":
    case "#buffer-size":
    case "#enhanced-session-detection":
      window.location.href = window.location.origin + "/Wavelet/Settings" + document.location.hash;
      break;
  }
</script>

# Quick start guide

You installed [Wavelet] but it doesn't seem to work out of the box... Try these steps to get started quickly!

- Most of the time you simply need to start playing some music before you're able to change settings in Wavelet
- Some music players don't work out of the box. Check out [Music player setup] and follow the steps for the music player you use (if it's listed)
- It is good practice to follow the instructions on [dontkillmyapp]. By completing the instructions, your device will allow Wavelet to detect music playback and not cause interruptions
- Check out the [Troubleshooting] page

[Wavelet]: https://play.google.com/store/apps/details?id=com.pittvandewitt.wavelet
[dontkillmyapp]: https://dontkillmyapp.com/
[Music player setup]: /Configuration
[Troubleshooting]: /Troubleshooting