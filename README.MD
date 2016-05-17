# **!!!!!!!! WARNINGS !!!!!!!!**

## **THIS REPOSITORY CONTAINS MALWARES!!!! DON'T DOWNLOAD OR RUN ANYTHING IN IT UNLESS YOU CLEARLY UNDERSTAND WHAT YOU ARE DOING!!!!**

# **！！！！ 警告 ！！！！**

## **該目錄下存有病毒程式！！！！ 請不要嘗試下載或運行裡面的任何程式，除非你非常清楚你在幹什麼！！！！**

# DCM Virus Samples

DCM is a Trojan Spy-ware dedicated to APT attack of specific targets.
It's first disclosed by Tecent's security team on Freebuf.<sup>[\[1\]][1]</sup>
It's developed by Chinese agency which rumored to be some g0v related
people. A self-claimed author member "DcmTeamMember" on V2EX posted
the insights about the creation of the virus.<sup>[\[2\]][2]</sup>

This repository contains some samples of the DCM virus collected from
various online virus sharing channels. The naming is the file's MD5
hash. If the original file is packed (usually with UPX) then an unpacked
version is provided for convinence.

#### `278ce79753aaa050fe750baba43490e5`

**Report:** http://r.virscan.org/report/fee007c110eeb4dfdba508120ab6bef4

This is the exact version used in the analysis article on Freebuf. So
I will personally refer it as `DCM-0`.

The resource files in the unpacked executable is encrypted with simple
XOR algorithm. (implemented in `sub_4011C0`) I added a decryption
script for your convinence. The extracted and decrypted resource files
are also included.

#### `1b7cd62b71235443cf267bd9104679dd`

**Report:** https://totalhash.cymru.com/analysis/?fbbbc68a4b56c9c70487753be3c26f4293e79ec9

This version has the same program structure as `DCM-0`. Even the
resource files are encrypted with the same algorithm. However the binary
seems to be a slightly larger than `DCM-0` thus I would guess it's an
upgraded version to `DCM-0`.

#### `261f4bbc423d79a1115840f300d5daf0`

**Report:** https://totalhash.cymru.com/analysis/?30161f778c28443b40b5cef76dc977b0c2c4c352

This version is another slightly changed `DCM-0`. It has less behaviour
characteristics on the report. I will categorize these 5 bin resources
silimar to `DCM-0` samples as `DCM-Δ`.

#### `89a5257fd9415b68ceab4a2122f70b45`

**Report:** https://totalhash.cymru.com/analysis/?823daa3fe3c32c32573b0317b488db901a191018

This version is basically the same as `DCM-0` with some minor changes.
I also contains 5 bin resources, thus is a `DCM-Δ`.

#### `82304a0a2ab419f657a4e9d8319c1e99`

**Report:** https://totalhash.cymru.com/analysis/?6f31aa2d01c5a67744fa8688933ae31dfc5a9c0d

This sample is reported to create mutex named `Global\I_AM_EXIST!!`,
which is an identifier of the DCM behaviour. However it lacks of any
other behaviour that a typical DCM virus should has. Therefore I think
it's actually an early or experimental version of `DCM-0`. It even doesn't
encrypt its resource files.

#### `1b2f0cbd3f048ee9f3e9885d4076ce8c`

**Report:** https://home.mcafee.com/virusinfo/virusprofile.aspx?key=2236045

I believe it's an early version DCM virus due to the small file size
with only two bin resources, and lack of most of the behaviour
characteristics of `DCM-0`. However, it does generate
`%TEMP%\{E53B9A13-F4C6-4d78-9755-65C029E88F02}\soft.prog` and other
core files that we can be certain that it's a variation of DCM.
Unlike `82304a0a2ab419f657a4e9d8319c1e99`, this version uses XOR encryption
for its resource files, but is slightly different than the algorithm used
in `DCM-0` in terms of parameters. Thus I think it's a development upgrade
of `82304a0a2ab419f657a4e9d8319c1e99`.

#### `1c37bcd907b6d574d9b204bbe5d4e4f6`

**Report:** https://www.virustotal.com/en/file/9eec021ab1e2d58d4e91dfbfc3d5c9239b206db7ec893c401335bd2654d673e7/analysis/

Yet another `DCM-Δ`.

#### `3e6aaf3e34ec2668c34c5ffe34b01b33`

**Report:** https://www.virustotal.com/en/file/fdacf92ff1f457ccb15eafe2fb49b982c8a723d0a98bd788bf7a1979cb0e717c/analysis/

Yet another `DCM-Δ`.

#### `4e90773b7e4adc5ff16e31f5d4942452`

**Report:** https://www.virustotal.com/en/file/9bf95a0f9ecbfcd981ed424c56bb633ed423f808856befc31b2e0453379f7340/analysis/

Yet another `DCM-Δ`.

#### `8b32eef5829507e469f294999a28ff23`

**Report:** https://www.virustotal.com/en/file/3f407180b2de4ebb9405836231b819953d5df3d3fa3a465ad4a2af8bae3cb2ad/analysis/

This one seems to be a further upgrade to `1b2f0cbd3f048ee9f3e9885d4076ce8c`
since they has the same bin resource encryption algorithm, but this one
has one more bin resource file implementing LSP hijacking.

#### `33c79e9a3cd9091f68de791fcf286a92`

**Report:** https://www.virustotal.com/en/file/c5130985605092aa0a812325b835ee8e3eed9fc7fcaaae329c1c24a241c797ec/analysis/

Yet another `DCM-Δ`.

#### `39adccebc7bb262731419128ec49f7bf`

**Report:** https://www.virustotal.com/en/file/73ffa5965a3ec44e9822bdb89b9bd8fa537985be11abab51616d3146287a64d0/analysis/

Yet another `DCM-Δ`.

#### `77f024dca6ce4401aa3f0c2fb293cbf6`

**Report:** https://www.virustotal.com/en/file/c727c3a11144c7b360cdb57ad46f399c3109b99dfee04a00cdbc8a5818452109/analysis/

Yet another `DCM-Δ`.

#### `305e64099e346cad595c08635a5558b6`

**Report:** https://www.virustotal.com/en/file/06c03eb8ccf561afe3cb15c0b1479e2095f3159e768d1a43aac26d77cc64f078/analysis/

This version is similar to `8b32eef5829507e469f294999a28ff23` since it
also contains 3 bin resources and uses the same encryption algorithm.

#### `577b7462d16600e0715f55a06cec6fb5`

**Report:** https://www.virustotal.com/en/file/a25f110437a60392fc075d15811d48efc8f20044d487e87dd69834a14a1fe831/analysis/

This version is similar to `8b32eef5829507e469f294999a28ff23` and
`305e64099e346cad595c08635a5558b6` since they both contain 3 bin
resources and use the same encryption algorithm.

#### `586afb4c3d03bdbacbc20b5ba73dd0eb`

**Report:** https://www.virustotal.com/en/file/5afc176cb56110413ecf8d2f595f17f7ccb1e44e6e124b5efdd82c83c2e8901b/analysis/

Yet another `DCM-Δ`.

#### `646f1297891ae9003cf42a3d0f166e6a`

**Report:** https://www.virustotal.com/en/file/2a20dda8eda2ee12837f103fb71bcef75478c21703936f12efcf4b35bade8fbb/analysis/

Yet another `DCM-Δ`.

#### `784c48011e6ce2a62c10542f99490768`

**Report:** https://www.virustotal.com/en/file/18fd1cc26dd416450e7aa44b7940bd760281a235783aad93bd4af3cc86609385/analysis/

Yet another `DCM-Δ`.

#### `95721afdb66fb239d95f7a9da3716bf0`

**Report:** https://www.virustotal.com/en/file/ffcb91932332ea701d72df4ae164f6e5196b9473d6db5e923baa6cb051974ae2/analysis/

Yet another `DCM-Δ`.

#### `148948adfea89ccbc4833c35147450bb`

**Report:** https://www.virustotal.com/en/file/9f0e0ca46316ada0b8906fbf4a4dc5e34b41b9acdab4bc99971c533b9d319fda/analysis/

Yet another `DCM-Δ`.

#### `c86dde45c416c717d2b12bfb3f37b44f`

**Report:** https://www.virustotal.com/en/file/43e02d3d8a7d8debbc8c023f37bfe5734dc247db162f9062d2517930892756a8/analysis/

Yet another `DCM-Δ`.

#### `ca67c7a1fa9f4ac51062ef34263b0a89`

**Report:** https://www.virustotal.com/en/file/a10099cbf6eeb5eaa0786ea83563ca155ce78e11f71647e8745f6392de8314c4/analysis/

This version is a bit strange since it lack of one x64 core DLL bin
resource file (bin/146) but contains other bin resources of `DCM-0`,
but it uses the encryption algorithm from `1b2f0cbd3f048ee9f3e9885d4076ce8c`.

#### `d30f83a62304eae90a152f96eed1eba1`

**Report:** https://www.virustotal.com/en/file/17a5d353364955cb1e4eb2fccfee1235f1a5e4cef1b15fa1f234d2dbfe198fcd/analysis/

Yet another `DCM-Δ`.

#### `dfd5efb790877d1edf459b95036b88fe`

**Report:** https://www.virustotal.com/en/file/1467cc7fc6fb9963ac5f9d3210465d4a73d2b22e5b425ac29056a36251bbc937/analysis/

Yet another `DCM-Δ`.

#### `fd9270e095f9efca801d839bfa6b5a11`

**Report:** https://www.virustotal.com/en/file/23808479f2a35fd60b80994c2d95a4e0087fd42ec6bb7ac4d83602280f4a3146/analysis/

Yet another `DCM-Δ`.

[1]: http://www.freebuf.com/articles/system/101447.html
[2]: https://www.v2ex.com/t/271590
