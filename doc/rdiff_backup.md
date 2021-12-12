# rdiff_backup_
This Munin plugin logs the rdiff_backup statistic data.
So you can easily see how many files were changed, removed, incremented or added.

## Installation
see [README.md](../README.md) for a general guide on how to install a munin plugin.

\* Please note that this is a wildcard plugin. See [Wildcard-Plugins](http://guide.munin-monitoring.org/en/latest/tutorial/wildcard-plugins.html) for more information.


## Dependencies
* python3
* python3-dateutil

## Configuration
Create a configuration file `rdiff_backup` in `/etc/munin/plugin-conf.d`. 
```config
[rdiff_backup_*]
    user root
    group root

[rdiff_backup_backupfolder]
    env.dir /path/to/backupfolder
```
