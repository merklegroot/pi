# Raspberry Pi Notes

## Assumptions

Most of these instructions are intended for the Raspberry Pi 400 running RaspberryPiOS.  

However, they're likely to still work on any Raspberry Pi running any Linux distribution with APT (Ubuntu, Debian, etc).  

## Bash Terminal

### Update the system

Update info about what's available.

``` bash
sudo apt update
```

Install those updates.

``` bash
sudo apt upgrade
```

## Terminal navigation

Where are we?

``` bash
# I always thought this looked "password", but nope
# it's "present working directory."
pwd
```

What's in our folder?

``` bash
ls
```

Who am I?

``` bash
whoami
```

What's my machine name?

``` bash
hostname
```

