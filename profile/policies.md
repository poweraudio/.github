Policies
--------

PowerAudio’s development activity is governed by the following policies:

1. The main focus of PowerAudio is to achieve software that builds and runs
   successfully on ppc64le GNU/Linux. In the case of audio plugins that can be
   compiled in multiple formats, [LV2] is the primary concern.
2. Only free/libre, open-source software is considered for porting.
3. Modifications made by PowerAudio are released under a free software license,
   generally the same license as the original.
4. Improvements that are good candidates for upstream inclusion (e.g.,
   uncontroversial fixes not specific to Power) are submitted as pull requests
   to the relevant repositories.
5. Where possible, if an issue on Power also affects other architectures, the
   fix is made as general as possible so that it benefits all architectures.
   For example, an x86-only program is ideally made cross-platform rather than
   adding support exclusively for Power.
6. Fixes for a specific architecture or platform should not adversely affect
   other system types that were previously working (e.g., a fix for `ppc64le`
   should not break `x86_64`).
7. Binary blobs are avoided. Even though [Waf] is free software, it is replaced
   with [autowaf] if distributed in binary form in any repository.

[LV2]: https://lv2plug.in/
[Waf]: https://waf.io/
[autowaf]: https://github.com/poweraudio/autowaf
