KU ITTC CCB Python Database scripts

#### Structure
- config.cfg     # configuration file for database scripts
- create-ccb.py  # creates the database
- update-ccb.py  # top-level database update script
- lib/           # third-party software
- plugins/       # database table update scripts (table name = script name)
- Makefile       # some useful commands
- README.md      # this readme file

##### To run the incremental updater manually:
- `python2 incremental_update_ccb.py 127.0.0.1 mysql-user mysql-pass`

##### To run the full updater manually:
- `python2 update_ccb.py 127.0.0.1 mysql-user mysql-pass`

#### Viewing log files:
- To see the log files generated by the updater, open the file 'config.cfg'.
- Look for a variable named 'logDir'.
- This directory is where the log files are stored.
- If you would like log files to be stored somewhere else, change the value of this variable.
- Feel free to delete or move any of these log files, they will be recreated by the updater
  the next time that it is run.

##### To clean up the directory tree (remove junk files)
- `make clean`

##### To restore up the directory tree (remove junk files and submodules)
- `make restore`
