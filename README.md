# Gnome time based mojave wallpaper

Mojave desert wallpaper useable as gnome background which changes during the day/night. 
Real scheludes with twenty minutes transitions.

Demo: https://imgur.com/a/fP2DplN

# Dependencies
* gnome-shell
* gnome-backgrounds

# Conflicts
* gnome-mojave-timed-wallpaper
* gnome-theme-macos-mojave-meta

# Installation
## Users of Arch Linux
Arch Linux users  need only clone and build this repository.

```
git clone https://github.com/japamax/gnome-mojave-timed-wallpaper.git
cd gnome-mojave-timed-wallpaper
makepkg -i
```

## Users of other distros
Users of other distros can manually complete these 3 steps:

1) Copy `mojave` directory from this repo  to `/usr/share/backgrounds/gnome` and make it readable by running the following as the root user:
```
mkdir -p /usr/share/backgrounds/gnome && 
cp -R mojave /usr/share/backgrounds/gnome && 
chmod 755 /usr/share/backgrounds/gnome/mojave && 
chmod 644 /usr/share/backgrounds/gnome/mojave/*
```

2) Copy `mojave-timed.xml` from this repo  to `/usr/share/backgrounds/gnome` and make it readable by running the following as the root user:
```
cp mojave-timed.xml /usr/share/backgrounds/gnome/mojave-timed.xml && 
chmod 644 /usr/share/backgrounds/gnome/mojave-timed.xml
```

3) Copy `mojave.xml` from this repo  to `/usr/share/gnome-background-properties` and make it readable by running the following as the root user:
```
mkdir -p /usr/share/gnome-background-properties && 
cp mojave.xml /usr/share/gnome-background-properties/mojave.xml && 
chmod 644 /usr/share/gnome-background-properties/mojave.xml
```
