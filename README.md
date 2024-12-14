# monark_updater
Checks for sd card activity and performs system updates if necessary.

# MONARK_Management (Software Updates)
`monark.py` also has an action type which is designed to run as a background service on the pi and periodically poll for sd card activity. If detected, it will take care of auto mounting and configuring for two cases:
1. If only a file called `update.zip` is present then it is mounted in readonly mode and the file will be extracted and the containing `update.sh` script will be executed.
2. Otherwise, the sd card will be mounted in read/write mode so that high res photos/videos can be saved on it.
