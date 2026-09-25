---
dg-publish: true
title: Mac Storage Optimization - Manually remove files
tags:
  - mac-storage-optimization
participants: Shristi Shrestha
---

- Display top ten files in the dir_path directory. Files are sorted by their size (in G)

```
du -sh {dir_path}/* | sort -rh | head -10
```


# Directories deleted to reduce storage from 20G to 150G

- Remove cache in the `~/Library` dir. The largest files.
	- `sudo rm -rf ~/Library/Caches/*`

- Remove **android** and **Xcode** log files. No active coding at the moment. 
	- `rm -rf ~/Library/Android/`
	- `rm -rf ~/Library/Developer/Xcode/DerivedData/*`

- Remove **claude** related caches
	- `rm -rf ~/Library/Application\ Support/Claude/clear`

- Remove **docker** related files
```
rm -rf ~/Library/Application\ Support/com.docker.install
rm -rf ~/.docker-compose 2>/dev/null
rm -rf ~/.docker 2>/dev/null
rm -rf ~/Library/Containers/com.docker.docker 2>/dev/null
```
