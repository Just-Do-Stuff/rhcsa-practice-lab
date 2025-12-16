Quick FileSystem Rules 

| Filesystem | Extend | Shrink |
|-----------|--------|--------|
| ext4 | Yes | Yes (unmount first) |
| xfs | Yes | NO |



## Notes

- Category 05 builds storage **correctly and persistently**
- Category 06 modifies or removes **what was built**
- Filesystem choice in Category 05 directly impacts Category 06 options
- Always verify mounts and swap after changes
