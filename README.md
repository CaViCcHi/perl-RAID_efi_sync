# raid_efi_sync
Something that will keep your /boot/efi synced between disks on your Linux Raid

It's pretty easy to configure, open the script 

change $basedir to whatever directory you want to be using as sync dir. Basically that's where the software will make a copy of /boot/efi for comparison and where it'll mount the backup efi partition in case it needs to sync

the other thing you need to change is @efiparts my 2 efi partitions are sda1 and sdb1 so you just need to put the name of your efi partitions. The order doesn't matter, the software will recognize which one is the one mounted and which ones are the backup.

once you made these 2 changes you can place the 2 scripts in the location shown in the tree

/etc/cron.d/raid_efi_sync_cron
/usr/local/bin/raid_efi_sync

The cron is configured to run every 5 minutes.
