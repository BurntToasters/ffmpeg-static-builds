BurntToasters: FFMPEG Notice
=============
## FFmpeg Static Build — Linked Components

The following libraries are statically linked into the FFmpeg binaries. Source code for all of them is included in this release.

### GPL-licensed

| Component | License | Source |
|-----------|---------|--------|
| FFmpeg | GPL-2.0-or-later | [git://git.ffmpeg.org/ffmpeg.git](https://git.ffmpeg.org/ffmpeg.git) |
| x264 | GPL-2.0-or-later | [https://code.videolan.org/videolan/x264](https://code.videolan.org/videolan/x264) |
| x265 | GPL-2.0-or-later | [https://bitbucket.org/multicoreware/x265_git](https://bitbucket.org/multicoreware/x265_git) |
| enca | GPL-2.0 | [https://dl.cihar.com/enca/](https://dl.cihar.com/enca/) |

### LGPL-licensed

| Component | License | Source |
|-----------|---------|--------|
| lame (libmp3lame) | LGPL-2.0 | [https://github.com/rbrito/lame](https://github.com/rbrito/lame) |
| fribidi | LGPL-2.1-or-later | [https://github.com/fribidi/fribidi](https://github.com/fribidi/fribidi) |
| libiconv | LGPL-2.1 | [https://ftp.gnu.org/pub/gnu/libiconv/](https://ftp.gnu.org/pub/gnu/libiconv/) |

### Permissive-licensed

| Component | License | Source |
|-----------|---------|--------|
| freetype | FTL / GPL-2.0 | [https://download.savannah.gnu.org/releases/freetype/](https://download.savannah.gnu.org/releases/freetype/) |
| fontconfig | MIT-like | [https://www.freedesktop.org/software/fontconfig/release/](https://www.freedesktop.org/software/fontconfig/release/) |
| libass | ISC | [https://github.com/libass/libass](https://github.com/libass/libass) |
| expat | MIT | [https://github.com/libexpat/libexpat](https://github.com/libexpat/libexpat) |

### Build tools (NOT linked into binaries — no source distribution required)

| Tool | License | Source |
|------|---------|--------|
| cmake | BSD-3-Clause | [https://cmake.org/download/](https://cmake.org/download/) |
| nasm | BSD-2-Clause | [https://www.nasm.us/pub/nasm/releasebuilds/](https://www.nasm.us/pub/nasm/releasebuilds/) |
| yasm | BSD-3-Clause | [http://www.tortall.net/projects/yasm/releases/](http://www.tortall.net/projects/yasm/releases/) |
| pkg-config | GPL-2.0 | [https://pkg-config.freedesktop.org/releases/](https://pkg-config.freedesktop.org/releases/) |

FFmpeg README
=============

FFmpeg is a collection of libraries and tools to process multimedia content
such as audio, video, subtitles and related metadata.

## Libraries

* `libavcodec` provides implementation of a wider range of codecs.
* `libavformat` implements streaming protocols, container formats and basic I/O access.
* `libavutil` includes hashers, decompressors and miscellaneous utility functions.
* `libavfilter` provides means to alter decoded audio and video through a directed graph of connected filters.
* `libavdevice` provides an abstraction to access capture and playback devices.
* `libswresample` implements audio mixing and resampling routines.
* `libswscale` implements color conversion and scaling routines.

## Tools

* [ffmpeg](https://ffmpeg.org/ffmpeg.html) is a command line toolbox to
  manipulate, convert and stream multimedia content.
* [ffplay](https://ffmpeg.org/ffplay.html) is a minimalistic multimedia player.
* [ffprobe](https://ffmpeg.org/ffprobe.html) is a simple analysis tool to inspect
  multimedia content.
* Additional small tools such as `aviocat`, `ismindex` and `qt-faststart`.

## Documentation

The offline documentation is available in the **doc/** directory.

The online documentation is available in the main [website](https://ffmpeg.org)
and in the [wiki](https://trac.ffmpeg.org).

### Examples

Coding examples are available in the **doc/examples** directory.

## License

FFmpeg codebase is mainly LGPL-licensed with optional components licensed under
GPL. Please refer to the LICENSE file for detailed information.

## Contributing

Patches should be submitted to the ffmpeg-devel mailing list using
`git format-patch` or `git send-email`. Github pull requests should be
avoided because they are not part of our review process and will be ignored.
