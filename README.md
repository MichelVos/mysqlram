# mysqlram
Run MySQL on a RAM disk for Linux

This includes a script you can run at boot or shutdown.
At boot time, it will copy the MySQL database to the RAM disk
At shutdown or reboot, it will copy the database from the RAM disk to disk
This might be a nice option to fight SD card wear on Raspberry Pis and clones.

## Installation
Copy mysqlram to /etc/init.d
Maybe it is necessary to chmod +x the file

Now run
```
sudo update-rc.d mysqlram defaults
```

## Warning
If a database runs on a RAM disk and the PC loses power, all changes since the last boot will be lost.
So use at your own risk.



