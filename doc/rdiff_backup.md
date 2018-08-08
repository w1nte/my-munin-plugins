# rdiff_backup_
This Munin Plugin logs the rdiff_backup statistic data.
So you can easily see how many files were changed, removed, incremented or added.

## Installation
see [README.md](../README.md)

## Dependencies
* python3
* python3-dateutil

## Configuration
Create a new file `rdiff_backup_` in `/etc/munin/plugin-conf.d`.
```config
[rdiff_backup_*]
    user root
    group root

[rdiff_backup_test]
    env.dir /path/to/backupfolder
```