# My Munin Plugins
All my munin plugins I developed.

##### Overview
* [rdiff_backup_](doc/rdiff_backup.md)

## Installation
#### Download Repository with Github (Recommended)
```bash
git clone https://github.com/w1nte/My-munin-plugins.git /usr/local/munin/lib/plugins/my-munin-plugins
```

#### Download single file
```bash
wget https://raw.githubusercontent.com/w1nte/My-munin-plugins/master/rdiff_backup_ /usr/local/munin/lib/plugins
```

## Configuration

#### Add plugin
Create a symbolic link to activate the plugin.
```bash
ln -s /usr/local/munin/lib/plugins/my-munin-plugins/rdiff_backup_ /etc/munin/plugins/rdiff_backup_Test
```

#### Change permission
Use `chmod a+x` to make the plugin executable.
```bash
chmod a+x /usr/local/munin/lib/plugins/my-munin-plugins/rdiff_backup_
```

#### Config the Plugin and satisfy the Dependencies.
* [rdiff_backup_](doc/rdiff_backup.md)

#### Restart Munin Node
```bash
service munin-node restart
```

#### Test the Plugin
```bash
munin-run -d rdiff_backup_Test
```