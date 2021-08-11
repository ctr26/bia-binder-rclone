[![Binder](https://binder.bioimagearchive.org/badge_logo.svg)](https://binder.bioimagearchive.org/v2/gh/ctr26/bia-binder-rclone/HEAD)

Demo binder environment for using rclone to mount external filesystems.

- `[start]` - We use to create the mounting dir and use `nohup` to push `rclone` into the background (fiddly to get right)
- `[environment.yml]` - We use conda to install the latest version of `rclone`
- `[apt.txt]` - To install `fuse` and and `libfuse`

This demo will only work on `https://binder.bioimagearchive.org/` as it mounts the `fuse` device at runtime [smart device manager](https://gitlab.com/arm-research/smarter/smarter-device-manager) provided by ARM

Please edit `.config/rclone/rclone.conf` to match the desired [filesystem](https://rclone.org/commands/rclone_config/) mounting, example here provided for [Biostudies](https://www.ebi.ac.uk/biostudies/)
