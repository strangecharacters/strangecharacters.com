---
title: "Ssd Failure"
date: 2023-03-06T17:11:55Z
draft: true
---

#### SSD Failure
Started this month with an unplanned project.
I got a cup of tea in the morning and turned my computer on to find 

/PXE error img/

The error indicates that the pc wasn't able to boot from the network. But it was only trying to boot from the network because it couldn't see any boot drive.

I opened the case and checked that the drives hadn't come physically loose ( they hadn't )

Then I created a live usb with linux so that  I could boot from an external drive.

I could list all the files on my boot (C:/) drive and all the files on my storage drive (D:/) as if nothing was wrong.

Restarting the machine gave the same error as before.

I thought if I can see the files but can't boot there must be something wrong with the boot sector of the drive so I created a windows installer on my usb drive.

Booting from that I tried to repair my windows installation but the installer had no success. 

I couldn't see what the problem was but I was resigned to reinstalling windows entirely.

But first, save what I could from the C: drive.

With the linux live usb I listed the files I needed and tried to copy them onto a backup drive. ( I was juggling drives like a master at this stage ) but straight away - error messages.
All my sttepts at copying resulted in failure.

I had assumed everything on the C: drive was intact except for the boot sector but it seems the rot went a little deeper.

I finally found someone describing similar symptoms to mine and they were saying that the physical drive was corrupt and was likely to only get worse. 

Thankfully most of the content I wanted to keep wasn't on my C: drive and I decided to remove the drive altogether and reinstall windows on my remaining drives.

So now I have a working computer. 

#### Backing up and down
I found the files I was most concerned about were on github, google photos, steam and in gmail which was helpful in this case but did make me think if I ever lost those accounts i'd be pretty screwed. I need to copy content down from the cloud as well as up. 