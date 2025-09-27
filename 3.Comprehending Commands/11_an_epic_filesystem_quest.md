## Challenge 11: 

The challenge is a small scavenger-hunt through the filesystem using ls, cd, and cat. 
A clue file in / points to another file/directory, and following the breadcrumbs 
eventually leads to the hidden flag.


## My Solve 
**Flag:**'pwn.college{gpE2G5VUev96BNcN-HTbsEQmPDW.QX5IDO0wiNyEzNzEzW}'

I followed the breadcrumb clues from /, using ls to discover clue files and cat to
read them, moving from one location to the next until I reached the final file 
containing the flag.
```
hacker@commands~an-epic-filesystem-quest:~$ cd /
hacker@commands~an-epic-filesystem-quest:/$ ls -a
.           TRACE  challenge  flag  lib32   media  opt   run   sys  var
..          bin    dev        home  lib64   mnt    proc  sbin  tmp
.dockerenv  boot   etc        lib   libx32  nix    root  srv   usr
hacker@commands~an-epic-filesystem-quest:/$ cat TRACE
Great sleuthing!
The next clue is in: /usr/share/doc/liblinear4
hacker@commands~an-epic-filesystem-quest:/$ ls -a /usr/share/doc/liblinear4
.  ..  README.Debian  README.gz  SNIPPET  changelog.Debian.gz  copyright
hacker@commands~an-epic-filesystem-quest:/$ cat /usr/share/doc/liblinear4/SNIPPET
Tubular find!
The next clue is in: /usr/share/doc/git/contrib/subtree

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/$ cd /usr/share/doc/git/contrib/subtree
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/git/contrib/subtree$ ls -a
.   BLUEPRINT  INSTALL   README       git-subtree.sh   t
..  COPYING    Makefile  git-subtree  git-subtree.txt  todo
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/git/contrib/subtree$ cat BLUEPRINT
Great sleuthing!
The next clue is in: /usr/share/racket/pkgs/srfi-lib/srfi/%3a41

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/git/contrib/subtree$ ls -a /usr/share/racket/pkgs/srfi-lib/srfi/%3a41
.  ..  SPOILER-TRAPPED  compiled  streams.rkt
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/git/contrib/subtree$ cat /usr/share/racket/pkgs/srfi-lib/srfi/%3a41/SPOILER-TRAPPED
Congratulations, you found the clue!
The next clue is in: /opt/linux/linux-5.4/drivers/media/i2c/adv748x

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/git/contrib/subtree$ ls -a /opt/linux/linux-5.4/drivers/media/i2c/adv748x
.  ..  .NOTE  Makefile  adv748x-afe.c  adv748x-core.c  adv748x-csi2.c  adv748x-hdmi.c  adv748x.h
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/git/contrib/subtree$ cat /opt/linux/linux-5.4/drivers/media/i2c/adv748x/.NOTE
Tubular find!
The next clue is in: /usr/lib/x86_64-linux-gnu/perl5/5.30

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/git/contrib/subtree$ cd /usr/lib/x86_64-linux-gnu/perl5/5.30
hacker@commands~an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/perl5/5.30$ ls -a
.  ..  INFO  Text  auto
hacker@commands~an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/perl5/5.30$ cat INFO
Great sleuthing!
The next clue is in: /usr/share/icons/hicolor/512x512/intl
hacker@commands~an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/perl5/5.30$ ls -a /usr/share/icons/hicolor/512x512/intl
.  ..  TEASER
hacker@commands~an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/perl5/5.30$ cat /usr/share/icons/hicolor/512x512/intl/TEASER
Great sleuthing!
The next clue is in: /opt/linux/linux-5.4/drivers/firmware/efi

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/perl5/5.30$ ls -a /opt/linux/linux-5.4/drivers/firmware/efi
.                .efi-bgrt.o.cmd  .memmap.o.cmd            .vars.o.cmd         arm-init.c        capsule.o          earlycon.c    efi.c      esrt.c      memattr.o     reboot.o            test
..               .efi.o.cmd       .reboot.o.cmd            Kconfig             arm-runtime.c     cper-arm.c         earlycon.o    efi.o      esrt.o      memmap.c      runtime-map.c       tpm.c
.built-in.a.cmd  .efivars.o.cmd   .runtime-map.o.cmd       Makefile            built-in.a        cper-x86.c         efi-bgrt.c    efibc.c    fake_mem.c  memmap.o      runtime-map.o       tpm.o
.capsule.o.cmd   .esrt.o.cmd      .runtime-wrappers.o.cmd  TIP-TRAPPED         capsule-loader.c  cper.c             efi-bgrt.o    efivars.c  libstub     rci2-table.c  runtime-wrappers.c  vars.c
.earlycon.o.cmd  .memattr.o.cmd   .tpm.o.cmd               apple-properties.c  capsule.c         dev-path-parser.c  efi-pstore.c  efivars.o  memattr.c   reboot.c      runtime-wrappers.o  vars.o
hacker@commands~an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/perl5/5.30$ cat /opt/linux/linux-5.4/drivers/firmware/efi/TIP-TRAPPED
Lucky listing!
The next clue is in: /usr/lib/python3/dist-packages/sympy/physics/optics/__pycache__

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/perl5/5.30$ ls -a /usr/lib/python3/dist-packages/sympy/physics/optics/__pycache__
.  ..  .SECRET  __init__.cpython-38.pyc  gaussopt.cpython-38.pyc  medium.cpython-38.pyc  polarization.cpython-38.pyc  utils.cpython-38.pyc  waves.cpython-38.pyc
hacker@commands~an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/perl5/5.30$ cat /usr/lib/python3/dist-packages/sympy/physics/optics/__pycache__/.SECRET
CONGRATULATIONS! Your perserverence has paid off, and you have found the flag!
It is: pwn.college{gpE2G5VUev96BNcN-HTbsEQmPDW.QX5IDO0wiNyEzNzEzW}
```

## What I Learned

How to proceed step-by-step with ls, cd, and cat to follow clues in the filesystem.
ls helps discover filenames; cat reads clue files. Combining them lets you follow breadcrumbs without guessing.
dotfiles may contain clues — use ls -a
Absolute paths are handy for reading a file from anywhere (cat /challenge/secret/flag) once you know its location.
Always be deliberate when moving around root (/) — use ls and cat rather than blind cd into random system dirs. 


## Incorrect Tangents

N/A


## References

N/A
