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
