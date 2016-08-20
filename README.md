zfs-auto-snapshot with the default crontabs running on 16.04 LTS.  This will auto snap every zfs filesystem you have with com.sun:auto-snapshot=true set.  https://github.com/zfsonlinux/zfs-auto-snapshot


Using with Docker Compose
--------------------------

```
  zfsautosnap:
    restart: always
    image: jayjanssen/zfs-auto-snapshot
    devices:
     - "/dev/zfs:/dev/zfs"
    volumes:
     - /etc/localtime:/etc/localtime:ro
```
