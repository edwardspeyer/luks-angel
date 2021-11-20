# luks-angel
* Unlock your LUKS cryptroot "automatically"
* Scan attached USB keys for LUKS keys
* Smite daemons from the bottomless pit at the [coming of the end-times](https://www.kingjamesbibleonline.org/Revelation-9-1/)
* Provision new USB keys for existing LUKS cryptroots


## Usage Diagram
<img src="angel.jpg" width="600" alt="Angel dealing with a daemon">


## Test Plan

It's important to test changes with the BusyBox shell and toolkit.  You can get
these from your local ramdisk:

```
d=$(mktemp -d)
(cd $d && zcat /initrd.img | cpio -i)
PATH=$d/bin ./luks-angel-keyscript
```
