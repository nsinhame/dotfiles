# My dotfiles

This directory contains the dotfiles for my system

## Requirements

Ensure you have the following installed on your system

### Git

```
pacman -S git
```

### Stow

```
pacman -S stow
```

## Installation

First, check out the dotfiles repo in your $HOME directory using git

```
$ git clone git@github.com/nsinhame/dotfiles.git
$ cd dotfiles
```

then use GNU stow to create symlinks

```
$ stow .
```


### For Brillo

Add following lines to /etc/udev/rules.d/backlight.rules

```
RUN+="/bin/chgrp wheel /sys/class/backlight/amdgpu_bl1/brightness"
RUN+="/bin/chmod g+w /sys/class/backlight/amdgpu_bl1/brightness"
```

and for intel

```
RUN+="/bin/chgrp wheel /sys/class/backlight/intel_backlight/brightness"
RUN+="/bin/chmod g+w /sys/class/backlight/intel_backlight/brightness"
```


