WebP Express 0.17.2. Conversion triggered using bulk conversion, 2019-12-08 07:25:11

*WebP Convert 2.3.0*  ignited.
- PHP version: 7.3.12
- Server software: LiteSpeed

Stack converter ignited

Options:
------------
The following options have been set explicitly. Note: it is the resulting options after merging down the "jpeg" and "png" options and any converter-prefixed options.
- source: [doc-root]/wp-content/uploads/2014/03/Jeff913print-531x400.png
- destination: [doc-root]/wp-content/webp-express/webp-images/doc-root/wp-content/uploads/2014/03/Jeff913print-531x400.png.webp
- log-call-arguments: true
- converters: (array of 9 items)

The following options have not been explicitly set, so using the following defaults:
- converter-options: (empty array)
- shuffle: false
- preferred-converters: (empty array)
- extra-converters: (empty array)

The following options were supplied and are passed on to the converters in the stack:
- alpha-quality: 85
- encoding: "auto"
- metadata: "none"
- near-lossless: 60
- quality: 85
------------


*Trying: cwebp* 

Options:
------------
The following options have been set explicitly. Note: it is the resulting options after merging down the "jpeg" and "png" options and any converter-prefixed options.
- source: [doc-root]/wp-content/uploads/2014/03/Jeff913print-531x400.png
- destination: [doc-root]/wp-content/webp-express/webp-images/doc-root/wp-content/uploads/2014/03/Jeff913print-531x400.png.webp
- alpha-quality: 85
- encoding: "auto"
- low-memory: true
- log-call-arguments: true
- metadata: "none"
- method: 6
- near-lossless: 60
- quality: 85
- use-nice: true
- command-line-options: ""
- try-common-system-paths: true
- try-supplied-binary-for-os: true

The following options have not been explicitly set, so using the following defaults:
- auto-filter: false
- default-quality: 85
- max-quality: 85
- preset: "none"
- size-in-percentage: null (not set)
- skip: false
- rel-path-to-precompiled-binaries: *****
- try-cwebp: true
- try-discovering-cwebp: true
------------

Encoding is set to auto - converting to both lossless and lossy and selecting the smallest file

Converting to lossy
Looking for cwebp binaries.
Discovering if a plain cwebp call works (to skip this step, disable the "try-cwebp" option)
- Executing: cwebp -version. Result: *Exec failed* (the cwebp binary was not found at path: cwebp)
Nope a plain cwebp call does not work
Discovering binaries using "which -a cwebp" command. (to skip this step, disable the "try-discovering-cwebp" option)
Found 0 binaries
Discovering binaries by peeking in common system paths (to skip this step, disable the "try-common-system-paths" option)
Found 0 binaries
Discovering binaries which are distributed with the webp-convert library (to skip this step, disable the "try-supplied-binary-for-os" option)
Checking if we have a supplied precompiled binary for your OS (Linux)... We do. We in fact have 3
Found 3 binaries: 
- [doc-root]/wp-content/plugins/webp-express/vendor/rosell-dk/webp-convert/src/Convert/Converters/Binaries/cwebp-103-linux-x86-64
- [doc-root]/wp-content/plugins/webp-express/vendor/rosell-dk/webp-convert/src/Convert/Converters/Binaries/cwebp-103-linux-x86-64-static
- [doc-root]/wp-content/plugins/webp-express/vendor/rosell-dk/webp-convert/src/Convert/Converters/Binaries/cwebp-061-linux-x86-64
Detecting versions of the cwebp binaries found
- Executing: [doc-root]/wp-content/plugins/webp-express/vendor/rosell-dk/webp-convert/src/Convert/Converters/Binaries/cwebp-103-linux-x86-64 -version. Result: *Exec failed*. Permission denied (user: "sparkl41" does not have permission to execute that binary)
- Executing: [doc-root]/wp-content/plugins/webp-express/vendor/rosell-dk/webp-convert/src/Convert/Converters/Binaries/cwebp-103-linux-x86-64-static -version. Result: *Exec failed*. Permission denied (user: "sparkl41" does not have permission to execute that binary)
- Executing: [doc-root]/wp-content/plugins/webp-express/vendor/rosell-dk/webp-convert/src/Convert/Converters/Binaries/cwebp-061-linux-x86-64 -version. Result: *Exec failed*. Permission denied (user: "sparkl41" does not have permission to execute that binary)

**Error: ** **No cwebp binaries could be executed (permission denied for user: "sparkl41").** 
No cwebp binaries could be executed (permission denied for user: "sparkl41").
cwebp failed in 122 ms

*Trying: vips* 

**Error: ** **Required Vips extension is not available.** 
Required Vips extension is not available.
vips failed in 0 ms

*Trying: imagemagick* 

**Error: ** **webp delegate missing** 
webp delegate missing
imagemagick failed in 31 ms

*Trying: graphicsmagick* 

Options:
------------
The following options have been set explicitly. Note: it is the resulting options after merging down the "jpeg" and "png" options and any converter-prefixed options.
- source: [doc-root]/wp-content/uploads/2014/03/Jeff913print-531x400.png
- destination: [doc-root]/wp-content/webp-express/webp-images/doc-root/wp-content/uploads/2014/03/Jeff913print-531x400.png.webp
- alpha-quality: 85
- encoding: "auto"
- log-call-arguments: true
- metadata: "none"
- quality: 85
- use-nice: true

The following options have not been explicitly set, so using the following defaults:
- default-quality: 85
- low-memory: false
- max-quality: 85
- method: 6
- skip: false

The following options were supplied but are ignored because they are not supported by this converter:
- near-lossless
------------

Encoding is set to auto - converting to both lossless and lossy and selecting the smallest file

Converting to lossy
Version: GraphicsMagick 1.3.20 2014-08-16 Q16 
Quality: 85. 
using nice
Executing command: nice gm convert -quality '85' -define webp:lossless=false -define webp:alpha-quality=85 -strip -define webp:method=6 '[doc-root]/wp-content/uploads/2014/03/Jeff913print-531x400.png' 'webp:[doc-root]/wp-content/webp-express/webp-images/doc-root/wp-content/uploads/2014/03/Jeff913print-531x400.png.webp.lossy.webp'
success
Reduction: 94% (went from 307 kb to 17 kb)

Converting to lossless
Version: GraphicsMagick 1.3.20 2014-08-16 Q16 
using nice
Executing command: nice gm convert -quality '85' -define webp:lossless=true -define webp:alpha-quality=85 -strip -define webp:method=6 '[doc-root]/wp-content/uploads/2014/03/Jeff913print-531x400.png' 'webp:[doc-root]/wp-content/webp-express/webp-images/doc-root/wp-content/uploads/2014/03/Jeff913print-531x400.png.webp.lossless.webp'
success
Reduction: 39% (went from 307 kb to 188 kb)

Picking lossy
graphicsmagick succeeded :)

Converted image in 1293 ms, reducing file size with 94% (went from 307 kb to 17 kb)
