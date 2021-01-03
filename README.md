# koarch, a simple arch installer script written in bash.
I make koarch mainly for myself, I had to install arch on a lot of computers at one point, so I stood up one night and wrote koarch to simplify my job greatly.
The installation steps are presented as a list and you usually would want to run them in order, but steps can be skipped or ran in a different order to fit your arch needs. You can go through the whole installation process without leaving the installer once (exceptions of course are when you chroot and reboot, just run `./koarch` to get back to bussiness) from ISO to complete GUI-install. I made it so it can support many computers, rn it can install arch on both x86_64 and x86_32 computers with either UEFI or Legacy boot protocols.
## getting koarch
koarch can be easily downloaded from my webapp, just connect your soon-to-be-arch computer to the internet via ethernet or usb android thetering and run:
### `pacman -S wget dialog ; wget koarch.netlify.app/koarch ; chmod +x koarch ; ./koarch`
you could also use curl for this.
## customizing the install
My goal for koarch is for it to be as universal as possible, to work on as many pcs as possible and for as many people as possible, so naturally I had to make the install very flexible. I added a `run command` optional step you can do at any time if you want something extra and implemented multiple DEs (gnome, plasma and xfce), I also got the partitioning step done with cfdisk, as that is much better and customizable than koarch could ever be (just keep in mind if your pc is legacy you need to pick dos in label type and make the root linux partition bootable, also you don't need a FAT32 UEFI partition).
# https://koarch.netlify.app/koarch

