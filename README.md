This is a an extension for Drive Badger. It provides `exclude.list` file, containing a list of exclusions compatible with popular `rsync` program.

The purpose of these exclusions is to decrease the amount of data to be exfiltrated by Drive Badger, and thus to speed up the attack,
by eliminating files and directories, that are not valuable in any way to the attacker:

- Android Studio
- Microsoft Visual Studio
- Microsoft SQL Server
- PostgreSQL pgAdmin
- VirtualBox
- various Jetbrains software
- various tools and SDKs

All rules are written and tested to exclude only irrelevant directories - eg. for Microsoft SQL Server, directories with application
files are excluded, but `DATA` directories containing `mdf` and `ldf` files are of course exfiltrated. And similarly for other rules.

### Installing

Clone this repository as `/opt/drivebadger/config/exclude-devel` directory on your Drive Badger persistent partition.

### More information

- [Drive Badger main repository](https://github.com/drivebadger/drivebadger)
- [Drive Badger wiki](https://github.com/drivebadger/drivebadger/wiki)
- [description, how configuration repositories work](https://github.com/drivebadger/drivebadger/wiki/Configuration-repositories)
