<h1 align="center">Rdiff-Backup Munin Plugin</h1>
<p align="center">This Munin plugin logs the rdiff_backup statistic data. So you can easily see how many files were changed, removed, incremented or added.</p>
<br>
<p align="center"><img src="./munin-plot.png?raw=true" height="300px"/></p>


## Installation
#### Download repository via Github (recommended)
```bash
git clone https://github.com/w1nte/rdiff-munin-plugin.git /usr/local/munin/lib/plugins/rdiff-munin-plugin
```

#### Or download single file
```bash
wget https://raw.githubusercontent.com/w1nte/rdiff-munin-plugin/master/rdiff_backup_ /usr/local/munin/lib/plugins
```

## Configuration

#### 1. Change permission
Use `chmod a+x` to make the plugin executable.
```bash
chmod a+x /usr/local/munin/lib/plugins/rdiff-munin-plugin/rdiff_backup_
```

#### 2. Enable plugin
Create a symbolic link `rdiff_backup_<folder>` in `/etc/munin/plugins/` for each backup folder *.
```bash
ln -s /usr/local/munin/lib/plugins/rdiff-munin-plugin/rdiff_backup_ /etc/munin/plugins/rdiff_backup_folder1
```
<sup>\* Please note that this is a wildcard plugin. See [Wildcard-Plugins](http://guide.munin-monitoring.org/en/latest/tutorial/wildcard-plugins.html) for more information.</sup>

#### 3. Configure plugins
Create a configuration file `rdiff_backup` in `/etc/munin/plugin-conf.d`. 
```config
[rdiff_backup_*]
    user root
    group root

[rdiff_backup_folder1]
    env.dir /path/to/backupfolder
```
#### 4. Install requirements
Install the dependencies if required:
* python3
* python3-dateutil

#### 5. Restart Munin-node
```bash
service munin-node restart
```

#### 6. Test the plugins
```bash
munin-run -d rdiff_backup_folder1
```
