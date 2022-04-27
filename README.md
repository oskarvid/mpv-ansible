# Ansible playbook for mpv and yt-dlp

## Instructions
* Change the username variable in `main.yml`
* Edit the `hosts` file
* Edit the `mpv.conf` file to your liking

## Comments
Apart from compiling `mpv` and installing `yt-dlp` the playbook is configured to benchmark 
each task.  Here's the execution time of my own `./rebuild.sh -j$(nproc)` runs:

| CPU | -j | Time |
|---|---|---|
| AMD Ryzen 7 5700U | -j16 | 3 minutes 28 seconds |
| AMD FX 8350 | -j8 | 3 minutes 28 seconds |
| Intel Core i5 10310U | -j8 | 4 minutes 30 seconds |
| Intel Core i5 2400 | -j4 | 5 minutes 24 seconds |
| Intel Core i3 6100T | -j4 | 6 minutes 18 seconds |
| Intel Core i5 5300U | -j4 | 7 minutes 10 seconds |
| Intel Core i5 6300U | -j4 | 7 minutes 45 seconds |
| Intel Core m3 7Y30 | -j4 | 9 minutes 28 seconds |
| Raspberry Pi 4 - 8GB | -j4 | 17 minutes 20 seconds |
| AMD Phenom X3 8400 | -j3 | 18 minutes 53 seconds |

The 2008 AMD Phenom X3 is 73 seconds slower than the 2019 Raspberry Pi 4 ARM CPU. In this case 
11 years of CPU development led to better performance from a 9 watt CPU than a 95 watt CPU. Amazing!
