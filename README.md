# docker-fedora-downgrade

```
docker run -it --net host -d -v /:/rootdir fedora:35
docker exec -it <docker-vm> bash

dnf install dnf-plugin-system-upgrade
dnf --installroot=/rootdir --exclude="kernel*" system-upgrade download --releasever=28 --allowerasing
```
