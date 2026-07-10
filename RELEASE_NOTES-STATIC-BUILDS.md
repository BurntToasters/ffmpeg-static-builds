This release provides precompiled fully static binaries of FFmpeg (`ffmpeg`, `ffplay`, and `ffprobe`) for Windows, Linux, and macOS.

To comply with the GNU General Public License (GPL) version 3.0 (which governs the combined work due to statically linking GPL and LGPL-3.0 libraries), the full source code of all compiled components is made available or linked below.

---

## FFmpeg Static Build — Linked Components & Credits

The precompiled static binaries link the following components:

### 1. GPL-Licensed Components

| Component | License | Source Repository / Homepage |
| :--- | :--- | :--- |
| **FFmpeg** (Core) | GPL-3.0-or-later | [https://git.ffmpeg.org/ffmpeg](https://git.ffmpeg.org/ffmpeg) |
| **x264** | GPL-2.0-or-later | [https://code.videolan.org/videolan/x264](https://code.videolan.org/videolan/x264) |
| **x265** | GPL-2.0-or-later | [https://bitbucket.org/multicoreware/x265_git](https://bitbucket.org/multicoreware/x265_git) |
| **vidstab** (libvidstab) | GPL-2.0-or-later | [https://github.com/georgmartius/vid.stab](https://github.com/georgmartius/vid.stab) |
| **frei0r** | GPL-2.0-or-later | [https://frei0r.dyne.org](https://frei0r.dyne.org) |
| **rubberband** | GPL-2.0-or-later | [https://breakfastquay.com/rubberband](https://breakfastquay.com/rubberband) |
| **xavs2** | GPL-2.0-or-later | [https://github.com/pkuvcl/xavs2](https://github.com/pkuvcl/xavs2) |
| **xvid** (libxvidcore) | GPL-2.0-or-later | [https://www.xvid.com](https://www.xvid.com) |
| **zvbi** | GPL-2.0-or-later | [https://sourceforge.net/projects/zapping](https://sourceforge.net/projects/zapping) |
| **enca** | GPL-2.0-only | [https://github.com/mharc/enca](https://github.com/mharc/enca) |
| **avisynth** (Windows only) | GPL-2.0-or-later | [https://github.com/AviSynth/AviSynthPlus](https://github.com/AviSynth/AviSynthPlus) |

### 2. LGPL-Licensed Components

| Component | License | Source Repository / Homepage |
| :--- | :--- | :--- |
| **lame** (libmp3lame) | LGPL-2.0-or-later | [https://lame.sourceforge.io](https://lame.sourceforge.io) |
| **fribidi** | LGPL-2.1-or-later | [https://github.com/fribidi/fribidi](https://github.com/fribidi/fribidi) |
| **libiconv** | LGPL-2.1-only | [https://www.gnu.org/software/libiconv](https://www.gnu.org/software/libiconv) |
| **libudfread** | LGPL-2.1-or-later | [https://code.videolan.org/videolan/libudfread](https://code.videolan.org/videolan/libudfread) |
| **libbluray** | LGPL-2.1-or-later | [https://code.videolan.org/videolan/libbluray](https://code.videolan.org/videolan/libbluray) |
| **gettext (libintl)** | LGPL-2.1-or-later | [https://www.gnu.org/software/gettext](https://www.gnu.org/software/gettext) |
| **libssh** | LGPL-2.1-or-later | [https://www.libssh.org](https://www.libssh.org) |
| **chromaprint** | LGPL-2.1-or-later | [https://github.com/acoustid/chromaprint](https://github.com/acoustid/chromaprint) |
| **libplacebo** | LGPL-2.1-or-later | [https://code.videolan.org/videolan/libplacebo](https://code.videolan.org/videolan/libplacebo) |
| **openal-soft** | LGPL-2.0-or-later | [https://openal-soft.org](https://openal-soft.org) |
| **soxr** (libsoxr) | LGPL-2.1-or-later | [https://sourceforge.net/projects/soxr](https://sourceforge.net/projects/soxr) |
| **twolame** | LGPL-2.1-or-later | [http://www.twolame.org](http://www.twolame.org) |
| **xz / liblzma** | LGPL-2.1-or-later | [https://tukaani.org/xz](https://tukaani.org/xz) |
| **gme** (Game Music Emu) | LGPL-2.1-or-later | [https://github.com/libgme/game-music-emu](https://github.com/libgme/game-music-emu) |
| **gmp** (GNU Multiple Precision) | LGPL-3.0-or-later | [https://gmplib.org](https://gmplib.org) |
| **libzmq** (ZeroMQ) | LGPL-3.0-or-later | [https://zeromq.org](https://zeromq.org) |

### 3. Permissive-Licensed Components (MIT, BSD, ISC, Zlib, WTFPL, Public Domain)

| Component | License | Source Repository / Homepage |
| :--- | :--- | :--- |
| **expat** | MIT | [https://github.com/libexpat/libexpat](https://github.com/libexpat/libexpat) |
| **libxml2** | MIT | [https://gitlab.gnome.org/GNOME/libxml2](https://gitlab.gnome.org/GNOME/libxml2) |
| **harfbuzz** | MIT-like | [https://harfbuzz.github.io](https://harfbuzz.github.io) |
| **whisper.cpp** | MIT | [https://github.com/ggerganov/whisper.cpp](https://github.com/ggerganov/whisper.cpp) |
| **openjpeg** | BSD-2-Clause | [https://github.com/uclouvain/openjpeg](https://github.com/uclouvain/openjpeg) |
| **kvazaar** | BSD-2-Clause | [https://github.com/ultravideo/kvazaar](https://github.com/ultravideo/kvazaar) |
| **vmaf** | BSD-2-Clause | [https://github.com/Netflix/vmaf](https://github.com/Netflix/vmaf) |
| **dav1d** | BSD-2-Clause | [https://code.videolan.org/videolan/dav1d](https://code.videolan.org/videolan/dav1d) |
| **openh264** | BSD-2-Clause | [https://www.openh264.org](https://www.openh264.org) |
| **libopus** (Opus) | BSD-3-Clause | [https://opus-codec.org](https://opus-codec.org) |
| **libogg** | BSD-3-Clause | [https://xiph.org/ogg](https://xiph.org/ogg) |
| **libvorbis** | BSD-3-Clause | [https://xiph.org/vorbis](https://xiph.org/vorbis) |
| **theora** (libtheora) | BSD-3-Clause | [https://theora.org](https://theora.org) |
| **snappy** | BSD-3-Clause | [https://github.com/google/snappy](https://github.com/google/snappy) |
| **libwebp** (WebP) | BSD-3-Clause | [https://developers.google.com/speed/webp](https://developers.google.com/speed/webp) |
| **libvpx** (VP8/VP9) | BSD-3-Clause | [https://www.webmproject.org](https://www.webmproject.org) |
| **aom** (libaom AV1) | BSD-3-Clause + Patent | [https://aomedia.googlesource.com/aom](https://aomedia.googlesource.com/aom) |
| **rav1e** | BSD-3-Clause | [https://github.com/xiph/rav1e](https://github.com/xiph/rav1e) |
| **openapv** | BSD-3-Clause | [https://github.com/isg-apv/openapv](https://github.com/isg-apv/openapv) |
| **openmpt** (libopenmpt) | BSD-3-Clause | [https://lib.openmpt.org/libopenmpt/](https://lib.openmpt.org/libopenmpt/) |
| **uavs3d** | BSD-3-Clause | [https://github.com/uavs3/uavs3d](https://github.com/uavs3/uavs3d) |
| **svt-av1** (SVT-AV1) | BSD-3-Clause-Clear | [https://gitlab.com/AOMediaCodec/SVT-AV1](https://gitlab.com/AOMediaCodec/SVT-AV1) |
| **lcevcdec** (MPEG-5 LCEVC) | BSD-3-Clause-Clear | [https://github.com/v-nova/lcevcdec](https://github.com/v-nova/lcevcdec) |
| **libass** | ISC | [https://github.com/libass/libass](https://github.com/libass/libass) |
| **zlib** | Zlib | [https://zlib.net](https://zlib.net) |
| **sdl2** (Simple DirectMedia Layer) | Zlib | [https://www.libsdl.org](https://www.libsdl.org) |
| **libpng** | Libpng | [http://www.libpng.org/pub/png/libpng.html](http://www.libpng.org/pub/png/libpng.html) |
| **zimg** (libzimg) | WTFPL | [https://github.com/sekrit-twc/zimg](https://github.com/sekrit-twc/zimg) |

### 4. Apache & MPL-Licensed Components

| Component | License | Source Repository / Homepage |
| :--- | :--- | :--- |
| **openssl** | Apache-2.0 | [https://www.openssl.org](https://www.openssl.org) |
| **opencore-amr** | Apache-2.0 | [https://sourceforge.net/projects/opencore-amr](https://sourceforge.net/projects/opencore-amr) |
| **libaribcaption** | Apache-2.0 | [https://github.com/xqq/libaribcaption](https://github.com/xqq/libaribcaption) |
| **srt** (Secure Reliable Transport) | MPL-2.0 | [https://github.com/Haivision/srt](https://github.com/Haivision/srt) |

### 5. Build Tools

| Tool | License | Source Repository / Homepage |
| :--- | :--- | :--- |
| **cmake** | BSD-3-Clause | [https://cmake.org](https://cmake.org) |
| **nasm** | BSD-2-Clause | [https://www.nasm.us](https://www.nasm.us) |
| **yasm** | BSD-3-Clause | [http://www.tortall.net/projects/yasm](http://www.tortall.net/projects/yasm) |
| **pkg-config** | GPL-2.0-or-later | [https://pkg-config.freedesktop.org](https://pkg-config.freedesktop.org) |
