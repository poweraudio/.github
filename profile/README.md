PowerAudio
==========

PowerAudio is a project that aims to port audio plugins to [IBM Power] systems
running GNU/Linux. The focus is on adding support for `ppc64le`—modern 64-bit
PowerPC running in little-endian mode—as this configuration has the highest
level of support in GNU/Linux distributions like [Debian], [Ubuntu], and
[Fedora].

[IBM Power]: https://en.wikipedia.org/wiki/IBM_Power_microprocessors
[Debian]: https://wiki.debian.org/ppc64el
[Ubuntu]: https://wiki.ubuntu.com/ppc64el
[Fedora]: https://fedoraproject.org/wiki/Architectures/PowerPC

Many ports also contain fixes and improvements for other processor
architectures, as well as GNU/Linux in general. Care is taken to ensure that
fixes for one architecture or platform do not adversely affect others.

Why?
----

Modern IBM Power systems have become more accessible to individuals due to the
offerings of companies like [Raptor Computing Systems]. As such, there is a
greater desire to run software geared toward personal use, such as audio
plugins, on this platform. In fact, most of the ports here were created because
I ([taylordotfish]) wanted to use those plugins on my own ppc64le machine.

[Raptor Computing Systems]: https://www.raptorcs.com/content/base/products.html
[taylordotfish]: https://github.com/taylordotfish

Status
------

Below is a summary of software ported by PowerAudio. These lists exclude
software for which all changes have been merged upstream, as well as
dependencies used only by a single program (see [PowerAudio’s repositories
page][repos] for a complete list).

[repos]: https://github.com/orgs/poweraudio/repositories

**Plugins:**

* [ArtyFX]: adds support for Power in build files.
* [Bitrot]: replaces binary blob, increases optimizations, and adds
  `--lv2-only` option.
* [DISTRHO Ports]: uses patched JUCE with Power fixes and adds support for
  non-x86/ARM to Vitalium and pitchedDelay.
* [DPF-Plugins]: allows choosing compiled plugin formats.
* [Dragonfly Reverb]: fixes VST 3 on Power and allows choosing plugin formats.
* [Helm]: fixes GCC errors, adds support for Power in build files, installs to
  `/usr/local`, and prevents unnecessary re-linking.
* [Monique]: uses patched JUCE with Power fixes, adds installation rules, and
  adds `LV2_ONLY` option.
* [Odin 2]: uses patched JUCE with Power fixes, adds installation rules, and
  adds `LV2_ONLY` option.
* [plugdata]: uses patched JUCE with Power fixes, installs to `/usr/local`
  (customizable), and adds `LV2_ONLY` option.
* [sfizz]: fixes GCC errors and updates dependency to version including Power
  fixes.
* [Surge XT]: uses patched JUCE with Power fixes, adds workaround if LuaJIT is
  unsupported, and adds `LV2_ONLY` option.
* [tap-lv2]: fixes build process on Power.
* [Triceratops]: replaces binary blob and increases optimization level.
* [Vaporizer2]: uses patched JUCE with Power fixes, adds support for
  non-x86/ARM, and adds `LV2_ONLY` option.
* [Wavetable] \(SocaLabs): uses patched JUCE with Power fixes, adds
  installation rules, disables non-free VST 2, and adds `LV2_ONLY` option.
* [Zyn-Fusion] \(ZynAddSubFX): installs to `/usr/local` (customizable), uses
  submodules, improves build process, and fixes LTO errors.

[ArtyFX]: https://github.com/poweraudio/openav-artyfx
[Bitrot]: https://github.com/poweraudio/bitrot
[DISTRHO Ports]: https://github.com/poweraudio/distrho-ports
[DPF-Plugins]: https://github.com/poweraudio/dpf-plugins
[Dragonfly Reverb]: https://github.com/poweraudio/dragonfly-reverb
[Helm]: https://github.com/poweraudio/helm
[Monique]: https://github.com/poweraudio/monique
[Odin 2]: https://github.com/poweraudio/odin2
[plugdata]: https://github.com/poweraudio/plugdata
[sfizz]: https://github.com/poweraudio/sfizz-ui
[Surge XT]: https://github.com/poweraudio/surge
[tap-lv2]: https://github.com/poweraudio/tap-lv2
[Triceratops]: https://github.com/poweraudio/triceratops
[Vaporizer2]: https://github.com/poweraudio/vaporizer2
[Wavetable]: https://github.com/poweraudio/socalabs-wavetable
[Zyn-Fusion]: https://github.com/poweraudio/zyn-fusion-build

**Libraries:**

* [autowaf]: adds branch with old `autowaf.py` but new Waf, sometimes needed
  when replacing blobs.
* [JUCE]: fixes linker errors on Power, adds fallback SIMD types on unsupported
  architectures, and fixes VST 3 generation on Power.
* [NTK]: replaces binary blob.
* [rust-lv2]: adds support for Power.

[autowaf]: https://github.com/poweraudio/autowaf
[JUCE]: https://github.com/poweraudio/JUCE
[NTK]: https://github.com/poweraudio/ntk
[rust-lv2]: https://github.com/poweraudio/rust-lv2

More information
----------------

For more information on PowerAudio’s approach to porting software, see the
[list of policies](policies.md) that govern development activity.

[This article on Talospace][talospace] further describes the history of
PowerAudio and the technical details of the porting process.

[talospace]:
 https://www.talospace.com/2024/09/music-production-on-power-adventure-in.html
