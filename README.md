# mysqlram
Run mysql on a RAM disk for linux

This contains a script that can be run at boot or shutdown.
At boot time it will copy the mysql database to ram disk
At shut down or reboot it will copy the database from ram disk to disk
This might be a nice option to fight sd card wear on raspberry-pi's and clones.

## Installation
Copy mysqlram to /etc/init.d
maybe it is necessary to chmod +x then file

Now run
```
sudo update-rc.d mysqlram defaults
```

## Warning
If a database is run on a RAM disk and the pc loses power all changes since the last boot will be lost.
So use on you own risk.



