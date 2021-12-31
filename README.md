# docker-fedora-downgrade
# System upgrade is only officially supported and tested over 2 releases at most (e.g. from 33 to 35). If you need to upgrade over more releases, it is recommended to do it in several smaller steps 
```

through docker run -it -d --net host -v /:/rootdir fedora:35
dnf install dnf-plugin-system-upgrade
dnf --installroot=/rootdir --exclude="kernel*" system-upgrade download --releasever=28 --allowerasing


natively 

dnf install dnf-plugin-system-upgrade
dnf --exclude="kernel*" system-upgrade download --releasever=28 --allowerasing


Transaction test succeeded.
Complete!
Transaction saved to /var/lib/dnf/system-upgrade/system-upgrade-transaction.json.
Download complete! Use 'dnf system-upgrade reboot' to start the upgrade.
To remove cached metadata and transaction use 'dnf system-upgrade clean'
The downloaded packages were saved in cache until the next successful transaction.
You can remove cached packages by executing 'dnf clean packages'.
```
