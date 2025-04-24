# Restic-UNRAID

This collection of scripts is to automate starting up a remote Unraid server which has an NFS export so that it can be a target for restic backup.  Once the backup is complete it will shut the server down.  
It will also wake up the server prior to start. 

The cron or scheduler will execute the command:


5 1 * * 1,4   /home/restic/command-file /home/restic/backup-r0-sources.txt

The text file is simply the backup collection moutn directories that you want to backup, mounted on the source system.

Examples (3 distinct mount points to backup).  This would be in the .txt file

/mnt/backup-ro/utilities
/mnt/backup-ro/scans
/mnt/backup-ro/archive

You will need to add ssh key to automatically backup, add the remote server name, it's MAC address, and the restic key
