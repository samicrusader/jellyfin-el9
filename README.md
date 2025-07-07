# Jellyfin RPM spec for Enterprise Linux 9

```bash
spectool -g jellyfin.spec
spectool -g jellyfin-ffmpeg.spec
./jellyfin-offline.sh
mock -r buildroot-node22.cfg --resultdir ../jellyfin-release/SRPMs --buildsrpm --sources . --spec jellyfin.spec
mock -r buildroot-node22.cfg --resultdir ../jellyfin-release/SRPMs --buildsrpm --sources . --spec jellyfin-ffmpeg.spec
mock -r buildroot-node22.cfg --resultdir ../jellyfin-release --rebuild ../jellyfin-release/SRPMs/*.src.rpm
```

thanks to @chenxiaolong for jellyfin-ffmpeg packaging: https://github.com/chenxiaolong/jellyfin-ffmpeg-fedora