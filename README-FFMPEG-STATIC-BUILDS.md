# FFmpeg Static Builds

This repository hosts the source code and distributes static builds of FFmpeg (`ffmpeg`, `ffplay`, and `ffprobe`) for Windows, Linux, and macOS. 

This file is persistent and documents the origins of the precompiled binaries, platform-specific setup instructions, and the required copyright/licensing credits for the statically linked components.

---

## Binary Origins

### 🖥️ Windows & Linux
Precompiled static binaries for Windows (x86_64) and Linux (x86_64) are retrieved from:
*   **BtbN/FFmpeg-Builds**: [Latest Releases](https://github.com/BtbN/FFmpeg-Builds/releases#release-latest)
*   These builds are compile-orchestrated via CI pipelines and include a comprehensive suite of external codecs and features.

### 🍏 macOS (Intel & Apple Silicon)
Static binaries for macOS are built using a custom Ramdisk compiler script located in the parent directory:
*   **macOS Static Builder**: `ffmpeg_osx-builder` (which mirrors static compilation instructions and compiler optimizations from [osxexperts.net](http://osxexperts.net)).
*   It isolates the compilation path to avoid dynamically linking host libraries (such as Homebrew or MacPorts), ensuring the resulting binaries are fully static and portable.

---

## Platform Setup & Troubleshooting

### 🍏 macOS Security (Quarantine & Codesign)
Modern macOS releases enforce strict gatekeeping. Because these static binaries are compiled locally/custom-built, you must manually register them with the system gatekeeper:

1.  **Remove Quarantine Flag**:
    If macOS displays a warning that the file "cannot be opened because developer cannot be verified," strip the quarantine extended attribute:
    ```bash
    xattr -dr com.apple.quarantine /path/to/ffmpeg
    xattr -dr com.apple.quarantine /path/to/ffplay
    xattr -dr com.apple.quarantine /path/to/ffprobe
    ```

2.  **Ad-Hoc Signing (Apple Silicon / ARM64)**:
    Apple Silicon Macs require all binary files to be codesigned. Run an ad-hoc signature to satisfy Apple's kernel requirements:
    ```bash
    codesign -s - /path/to/ffmpeg
    codesign -s - /path/to/ffplay
    codesign -s - /path/to/ffprobe
    ```

### 🖥️ Windows Requirements
*   **Universal C Runtime (UCRT)**: The Windows binaries compiled by BtbN require Microsoft's UCRT (standard on Windows 10 and 11). If run on older Windows versions, you may need to install the UCRT redistributable package.

---

## Statically Linked Components & Credits

Since the distributed binaries are statically linked, they embed code from numerous external libraries. In accordance with their respective licenses (GPL, LGPL, Apache, BSD, MIT, etc.), the following tables provide credits and links to the source codes of all compiled components.

Because some optional components are licensed under the GPL-2.0/GPL-3.0 or LGPL-3.0, the combined binary distribution is governed by the **GNU General Public License (GPL) version 3.0**.

### 1. GPL-Licensed Components
These libraries require that the source code of the combined work be distributed under GPL terms.

| Library | License | Source Repository / Homepage |
| :--- | :--- | :--- |
| **FFmpeg** (Core) | GPL-3.0-or-later | [git.ffmpeg.org](https://git.ffmpeg.org/ffmpeg) |
| **x264** | GPL-2.0-or-later | [videolan.org/x264](https://code.videolan.org/videolan/x264) |
| **x265** | GPL-2.0-or-later | [bitbucket.org/multicoreware/x265_git](https://bitbucket.org/multicoreware/x265_git) |
| **vidstab** (libvidstab) | GPL-2.0-or-later | [github.com/georgmartius/vid.stab](https://github.com/georgmartius/vid.stab) |
| **frei0r** | GPL-2.0-or-later | [frei0r.dyne.org](https://frei0r.dyne.org) |
| **rubberband** | GPL-2.0-or-later | [breakfastquay.com/rubberband](https://breakfastquay.com/rubberband) |
| **xavs2** | GPL-2.0-or-later | [github.com/pkuvcl/xavs2](https://github.com/pkuvcl/xavs2) |
| **xvid** (libxvidcore) | GPL-2.0-or-later | [xvid.com](https://www.xvid.com) |
| **zvbi** | GPL-2.0-or-later | [sourceforge.net/projects/zapping](https://sourceforge.net/projects/zapping) |
| **enca** | GPL-2.0-only | [github.com/mharc/enca](https://github.com/mharc/enca) |
| **avisynth** (Windows only) | GPL-2.0-or-later | [github.com/AviSynth/AviSynthPlus](https://github.com/AviSynth/AviSynthPlus) |

### 2. LGPL-Licensed Components
These components are licensed under the LGPL and are statically linked into the binaries.

| Library | License | Source Repository / Homepage |
| :--- | :--- | :--- |
| **lame** (libmp3lame) | LGPL-2.0-or-later | [lame.sourceforge.io](https://lame.sourceforge.io) |
| **fribidi** | LGPL-2.1-or-later | [github.com/fribidi/fribidi](https://github.com/fribidi/fribidi) |
| **libiconv** | LGPL-2.1-only | [gnu.org/software/libiconv](https://www.gnu.org/software/libiconv) |
| **libudfread** | LGPL-2.1-or-later | [code.videolan.org/videolan/libudfread](https://code.videolan.org/videolan/libudfread) |
| **libbluray** | LGPL-2.1-or-later | [code.videolan.org/videolan/libbluray](https://code.videolan.org/videolan/libbluray) |
| **gettext (libintl)** | LGPL-2.1-or-later | [gnu.org/software/gettext](https://www.gnu.org/software/gettext) |
| **libssh** | LGPL-2.1-or-later | [libssh.org](https://www.libssh.org) |
| **chromaprint** | LGPL-2.1-or-later | [github.com/acoustid/chromaprint](https://github.com/acoustid/chromaprint) |
| **libplacebo** | LGPL-2.1-or-later | [code.videolan.org/videolan/libplacebo](https://code.videolan.org/videolan/libplacebo) |
| **openal-soft** | LGPL-2.0-or-later | [openal-soft.org](https://openal-soft.org) |
| **soxr** (libsoxr) | LGPL-2.1-or-later | [sourceforge.net/projects/soxr](https://sourceforge.net/projects/soxr) |
| **twolame** | LGPL-2.1-or-later | [twolame.org](http://www.twolame.org) |
| **xz / liblzma** | LGPL-2.1-or-later | [tukaani.org/xz](https://tukaani.org/xz) |
| **gme** (Game Music Emu) | LGPL-2.1-or-later | [github.com/libgme/game-music-emu](https://github.com/libgme/game-music-emu) |
| **gmp** (GNU Multiple Precision) | LGPL-3.0-or-later | [gmplib.org](https://gmplib.org) |
| **libzmq** (ZeroMQ) | LGPL-3.0-or-later | [zeromq.org](https://zeromq.org) |

### 3. Permissive-Licensed Components
These libraries are licensed under permissive terms (MIT, BSD, ISC, Zlib, WTFPL, Public Domain).

| Library | License | Source Repository / Homepage |
| :--- | :--- | :--- |
| **expat** | MIT | [github.com/libexpat/libexpat](https://github.com/libexpat/libexpat) |
| **libxml2** | MIT | [gitlab.gnome.org/GNOME/libxml2](https://gitlab.gnome.org/GNOME/libxml2) |
| **harfbuzz** | MIT-like | [harfbuzz.github.io](https://harfbuzz.github.io) |
| **whisper.cpp** | MIT | [github.com/ggerganov/whisper.cpp](https://github.com/ggerganov/whisper.cpp) |
| **openjpeg** | BSD-2-Clause | [github.com/uclouvain/openjpeg](https://github.com/uclouvain/openjpeg) |
| **kvazaar** | BSD-2-Clause | [github.com/ultravideo/kvazaar](https://github.com/ultravideo/kvazaar) |
| **vmaf** | BSD-2-Clause | [github.com/Netflix/vmaf](https://github.com/Netflix/vmaf) |
| **dav1d** | BSD-2-Clause | [code.videolan.org/videolan/dav1d](https://code.videolan.org/videolan/dav1d) |
| **openh264** | BSD-2-Clause | [openh264.org](https://www.openh264.org) |
| **libopus** (Opus) | BSD-3-Clause | [opus-codec.org](https://opus-codec.org) |
| **libogg** | BSD-3-Clause | [xiph.org/ogg](https://xiph.org/ogg) |
| **libvorbis** | BSD-3-Clause | [xiph.org/vorbis](https://xiph.org/vorbis) |
| **theora** (libtheora) | BSD-3-Clause | [theora.org](https://theora.org) |
| **snappy** | BSD-3-Clause | [github.com/google/snappy](https://github.com/google/snappy) |
| **libwebp** (WebP) | BSD-3-Clause | [developers.google.com/speed/webp](https://developers.google.com/speed/webp) |
| **libvpx** (VP8/VP9) | BSD-3-Clause | [webmproject.org](https://www.webmproject.org) |
| **aom** (libaom AV1) | BSD-3-Clause + Patent | [aomedia.googlesource.com/aom](https://aomedia.googlesource.com/aom) |
| **rav1e** | BSD-3-Clause | [github.com/xiph/rav1e](https://github.com/xiph/rav1e) |
| **openapv** | BSD-3-Clause | [github.com/isg-apv/openapv](https://github.com/isg-apv/openapv) |
| **openmpt** (libopenmpt) | BSD-3-Clause | [lib.openmpt.org](https://lib.openmpt.org/libopenmpt) |
| **uavs3d** | BSD-3-Clause | [github.com/uavs3/uavs3d](https://github.com/uavs3/uavs3d) |
| **svt-av1** (SVT-AV1) | BSD-3-Clause-Clear | [gitlab.com/AOMediaCodec/SVT-AV1](https://gitlab.com/AOMediaCodec/SVT-AV1) |
| **lcevcdec** (MPEG-5 LCEVC) | BSD-3-Clause-Clear | [github.com/v-nova/lcevcdec](https://github.com/v-nova/lcevcdec) |
| **libass** | ISC | [github.com/libass/libass](https://github.com/libass/libass) |
| **zlib** | Zlib | [zlib.net](https://zlib.net) |
| **sdl2** (Simple DirectMedia Layer) | Zlib | [libsdl.org](https://www.libsdl.org) |
| **libpng** | Libpng | [libpng.org](http://www.libpng.org/pub/png/libpng.html) |
| **zimg** (libzimg) | WTFPL | [github.com/sekrit-twc/zimg](https://github.com/sekrit-twc/zimg) |

### 4. Apache & MPL-Licensed Components
These libraries are compiled and linked under either the Apache 2.0 or Mozilla Public License 2.0.

| Library | License | Source Repository / Homepage |
| :--- | :--- | :--- |
| **openssl** | Apache-2.0 | [openssl.org](https://www.openssl.org) |
| **opencore-amr** | Apache-2.0 | [sourceforge.net/projects/opencore-amr](https://sourceforge.net/projects/opencore-amr) |
| **libaribcaption** | Apache-2.0 | [github.com/xqq/libaribcaption](https://github.com/xqq/libaribcaption) |
| **srt** (Secure Reliable Transport) | MPL-2.0 | [github.com/Haivision/srt](https://github.com/Haivision/srt) |

### 5. Build Tools
The following tools are used during compilation but are NOT linked into the distributed binaries. No source code redistribution is required for these.

| Tool | License | Source Repository / Homepage |
| :--- | :--- | :--- |
| **cmake** | BSD-3-Clause | [cmake.org](https://cmake.org) |
| **nasm** | BSD-2-Clause | [nasm.us](https://www.nasm.us) |
| **yasm** | BSD-3-Clause | [tortall.net/projects/yasm](http://www.tortall.net/projects/yasm) |
| **pkg-config** | GPL-2.0-or-later | [pkg-config.freedesktop.org](https://pkg-config.freedesktop.org) |
