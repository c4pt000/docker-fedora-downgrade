# docker-fedora-downgrade

```


dnf install dnf-plugin-system-upgrade
dnf --installroot=/rootdir --exclude="kernel*" system-upgrade download --releasever=28 --allowerasing
```
