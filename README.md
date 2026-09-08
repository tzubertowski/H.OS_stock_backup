# H.OS stock backups

Clean, minimal stock firmware SD card backups for H.OS handheld consoles. These
archives restore the original system files needed before installing TreeFrogUI;
commercial game ROMs are not included.

## Supported consoles

- R36SX v2.6
- R36SX v2.7
- R36HD (uses the R36SX v2.6 base)
- SF3000
- SF3000 HD
- SF3100
- SF3500
- GB350

Download the matching stock firmware backup from this repository's
[releases](../../releases). Each archive is intended for its named console only;
do not use a backup for a different model or hardware revision, except for the
tested R36HD installation path described below.

For **R36HD**, select R36HD in the TreeFrogUI installer. It restores
`R36SX_v2.6_stock.7z` and then applies the dedicated R36HD device overlay. The
factory R36HD/R36SX v2.7 protected menu binary stalls at the TreeFrogUI logo and
must not be used as the installation base.

These H.OS stock SD card backups are mirrored in one place for reliable use by
the TreeFrogUI installer and for manual recovery of supported handhelds.

## Clean stock backups (TreeFrogUI-optimized)

Besides the full stock backups above, cleaned variants are available in the
[`clean-stock-v1`](../../releases/tag/clean-stock-v1) release. They contain the
same stock system files required by the TreeFrogUI installer, with console data
that TreeFrogUI does not need removed, for a cleaner installation:

- stock save data, high scores and save states (`cubegm/saves`,
  `cubegm/states`, `.sav`, `.nv`, `.hi`, `.ps0`, `.sv0` files, `mame2000`
  nvram/memcard/snap data)
- factory per-game cheat files where present (`cubegm/cheat`)
- empty ROM/media folder skeletons (ATARI, FC, GB, GBA, GBC, GG, MAME, MD,
  Movie, Music, NGPC, PCE, PS, Photo, SFC, SMS, WSC, Ebook, BGM)
- built-in stock emulator cores (`cubegm/cores/libemu_*.so`), which TreeFrogUI
  replaces with its own core set

No commercial game ROMs are included; none are present in these archives. The
stock boot/menu binaries and root file system needed as the installation base
are preserved, so the TreeFrogUI installer (which locates the `cubegm/`
directory inside the extracted archive) works with both variants.

### Files and SHA-256 checksums

| Console | File | Size | SHA-256 |
|---|---|---|---|
| R36SX v2.6 | [`R36SX_v2.6_cleanstock.7z`](../../releases/download/clean-stock-v1/R36SX_v2.6_cleanstock.7z) | 68.2 MiB | `0ef6ecb1767c0d837e6b943b931716fd0322f4d4268d759e9e78d5fea39a8b22` |
| R36SX v2.7 | [`R36SX_v2.7_cleanstock.7z`](../../releases/download/clean-stock-v1/R36SX_v2.7_cleanstock.7z) | 97.2 MiB | `44f57a338516e8dcb76c68d8037361f5465f94cc85cbb6b36d5202d445586d82` |
| R36HD | [`R36HD_cleanstock.7z`](../../releases/download/clean-stock-v1/R36HD_cleanstock.7z) | 103.4 MiB | `638c242fea3b7b650f155a3d3e2ab78205524c1a181e1daabda471b2e1c6fdc9` |
| SF3000 | [`SF3000_cleanstock.7z`](../../releases/download/clean-stock-v1/SF3000_cleanstock.7z) | 63.9 MiB | `f1001723f84910d64bf2ae5620d891840202d281b101b7a067ee48a0a38ac9d5` |
| SF3000 HD | [`SF3000_HD_cleanstock.7z`](../../releases/download/clean-stock-v1/SF3000_HD_cleanstock.7z) | 62.7 MiB | `d22a64acde2436b633be47a436659a2d1e9af84af4405477c8cfc48bed4bbfd3` |
| SF3100 | [`SF3100_cleanstock.7z`](../../releases/download/clean-stock-v1/SF3100_cleanstock.7z) | 65.3 MiB | `0ddb91c5e146767cc2a9692b4ab63285627c85b1a436a48bd8d62f4381c492ba` |
| SF3500 | [`SF3500_cleanstock.7z`](../../releases/download/clean-stock-v1/SF3500_cleanstock.7z) | 59.1 MiB | `faea1d6b8ec42d948ed0657b0035a0cc732299495c6dccc685a57b0dac1d5b9f` |
| GB350 | [`GB350_cleanstock.7z`](../../releases/download/clean-stock-v1/GB350_cleanstock.7z) | 63.5 MiB | `3a96d71da7145988c77f60f529f0cbc7a650255f4ed96676003d8e5692893e10` |

> Note: the R36HD clean stock backup keeps the full R36HD stock root (including
> its protected menu binary) for recovery purposes; the TreeFrogUI installer
> still installs R36HD from the R36SX v2.6 base plus the R36HD overlay, exactly
> as described above.
