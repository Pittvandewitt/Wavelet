# Import custom AutoEq data in Wavelet

The import feature allows you to use your own created compensation data in Wavelet, which is useful if your headphone model is not listed or if you wish to tweak the current result shipped with Wavelet.  

 [AutoEq.app](https://autoeq.app){ .md-button }  
*Visit autoeq.app to get started.*  

Wavelet will use the file name (without extension) of the GraphicEq file to display your imported result.  
Currently, the GraphicEQ file must meet the following format to be accepted by Wavelet:

```
GraphicEQ: 20 0; 21 0; 22 0; 23 0; 24 0; 26 0; 27 0; 29 0; 30 0; 32 0; 34 0; 36 0; 38 0; 40 0; 43 0; 45 0; 48 0; 50 0; 53 0; 56 0; 59 0; 63 0; 66 0; 70 0; 74 0; 78 0; 83 0; 87 0; 92 0; 97 0; 103 0; 109 0; 115 0; 121 0; 128 0; 136 0; 143 0; 151 0; 160 0; 169 0; 178 0; 188 0; 199 0; 210 0; 222 0; 235 0; 248 0; 262 0; 277 0; 292 0; 309 0; 326 0; 345 0; 364 0; 385 0; 406 0; 429 0; 453 0; 479 0; 506 0; 534 0; 565 0; 596 0; 630 0; 665 0; 703 0; 743 0; 784 0; 829 0; 875 0; 924 0; 977 0; 1032 0; 1090 0; 1151 0; 1216 0; 1284 0; 1357 0; 1433 0; 1514 0; 1599 0; 1689 0; 1784 0; 1885 0; 1991 0; 2103 0; 2221 0; 2347 0; 2479 0; 2618 0; 2766 0; 2921 0; 3086 0; 3260 0; 3443 0; 3637 0; 3842 0; 4058 0; 4287 0; 4528 0; 4783 0; 5052 0; 5337 0; 5637 0; 5955 0; 6290 0; 6644 0; 7018 0; 7414 0; 7831 0; 8272 0; 8738 0; 9230 0; 9749 0; 10298 0; 10878 0; 11490 0; 12137 0; 12821 0; 13543 0; 14305 0; 15110 0; 15961 0; 16860 0; 17809 0; 18812 0; 19871 0
```

Adding, changing or removing frequencies will lead to an incompable file. This format might change in the future if the output from AutoEq changes. It is highly recommended to save the CSV file you created, so you can rerun the calculations to easily adapt your custom compensation data to a new format.

[Equalizing Headphones the Easy Way]: https://medium.com/@jaakkopasanen/make-your-headphones-sound-supreme-1cbd567832a9
[AutoEq]: https://github.com/jaakkopasanen/AutoEq