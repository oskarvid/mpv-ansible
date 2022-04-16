# Ansible playbook for mpv and yt-dlp

## Instructions
* Change the username variable in `main.yml`
* Edit the `hosts` file
* Edit the `mpv.conf` file to your liking
* Edit the `-j4` flag in the "Execute the rebuild script" task to your number of CPU threads

## Comments
Apart from compiling `mpv` and installing `yt-dlp` the playbook is configured to benchmark each task.  
Here's the execution time of my own runs:  

| CPU | -j | Time |
|---|---|---|
| Ryzen 7 5700U | -j16 | 3 minutes 28 seconds |
| Intel Core i3 6100T | -j4 | 6 minutes 18 seconds |
| Intel Core i5 6300U | -j4 | 7 minutes 45 seconds |
| Intel Core i5 10310U | -j8 | 4 minutes 30 seconds |
