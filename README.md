# Time based GNOME macOS Mojave wallpaper with real scheludes</br>& Azimuth Elevation based KDE macOS Mojave wallpaper

Mojave dynamic wallpaper is 16 based images wallpaper.</br>
Mojave dynamic wallpaper is useable as Gnome/KDE background which changes during the day/night.</br>
For Gnome, it's a timed based wallpaper with real scheludes with 30 minutes transitions.</br>
For KDE, the 1st version is a Azimuth Elevation wallpaper based on real Azimuth Elevation of the Sun for the Mojave Kelso Dunes on 21/06/2019.</br>
For KDE, the 2nd version is  a timed based wallpaper with real scheludes.</br></br>


<p align="center">
  <img width="480" height="270" src="gnome-kde-dynamic-wallpaper-mojave.gif">
</p>


# Dependencies
* Gnome
  * gnome-shell
  * gnome-backgrounds
* KDE
  * plasma5-wallpapers-dynamic for Archlinux 
  * or [home: KAMiKAZOW:KDE](https://software.opensuse.org//download.html?project=home%3AKAMiKAZOW%3AKDE&package=plasma5-dynamic-wallpaper) for Opensuze
  - or [GitHub: zzag/dynamic-wallpaper](https://github.com/zzag/dynamic-wallpaper) for others distros

# Parameters
## Gnome
None but you must sync your system clock time (presented both in local time and UTC) as well as the RTC (hardware clock).
## KDE
Select "Dynamic" wallpaper type, put your real coordinates and your timer for thz solar version.


# Installation
## Users of Arch Linux
Arch Linux users  need only clone and build this repository.

```
git clone https://github.com/japamax/gnome-kde-mojave-dynamic-wallpaper.git
cd gnome-kde-mojave-dynamic-wallpaper
makepkg -si
```

## Users of other distros
Users of other distros can manually complete these 7 steps:

1) Copy `mojave` directory from this repo  to `/usr/share/dynamicwallpapers/mojave-solar/contents/images` and make it readable by running the following as the root user:
```
mkdir -p /usr/share/dynamicwallpapers/mojave-solar/contents/images && 
cp mojave/* /usr/share/dynamicwallpapers/mojave-solar/contents/images && 
chmod 755 /usr/share/dynamicwallpapers/mojave-solar/contents/images && 
chmod 644 /usr/share/dynamicwallpapers/mojave-solar/contents/images/*
```

2) Create `/usr/share/dynamicwallpapers/mojave-timed/contents/images` and make it readable by running the following as the root user:
```
mkdir -p /usr/share/dynamicwallpapers/mojave-timed/contents && 
chmod 755 /usr/share/dynamicwallpapers/mojave-timed/contents  && 
ln -s /usr/share/dynamicwallpapers/mojave-solar/contents/images /usr/share/dynamicwallpapers/mojave-timed/contents/images 
```


3) Link `mojave` directory from `/usr/share/dynamicwallpapers` to `/usr/share/backgrounds/macOS` by running the following as the root user:
```
mkdir -p /usr/share/backgrounds/macOS &&
ln -s /usr/share/dynamicwallpapers/mojave-solar/contents/images /usr/share/backgrounds/macOS/mojave
```

4) Copy `mojave-solar.json` from this repo  to `/usr/share/dynamicwallpapers/mojave-solar/metadata.json` and make it readable by running the following as the root user:
```
cp mojave-solar.json /usr/share/dynamicwallpapers/mojave-solar/metadata.json && 
chmod 644 /usr/share/dynamicwallpapers/mojave-solar/metadata.json
```

5) Copy `mojave-timed.json` from this repo  to `/usr/share/dynamicwallpapers/mojave-timed/metadata.json` and make it readable by running the following as the root user:
```
cp mojave-timed.json /usr/share/dynamicwallpapers/mojave-timed/metadata.json && 
chmod 644 /usr/share/dynamicwallpapers/mojave-timed/metadata.json
```

6) Copy `mojave-timed.xml` from this repo  to `/usr/share/backgrounds/macOS` and make it readable by running the following as the root user:
```
cp mojave-timed.xml /usr/share/backgrounds/macOS/mojave-timed.xml && 
chmod 644 /usr/share/backgrounds/macOS/mojave-timed.xml
```

7) Copy `mojave.xml` from this repo  to `/usr/share/gnome-background-properties` and make it readable by running the following as the root user:
```
mkdir -p /usr/share/gnome-background-properties && 
cp mojave.xml /usr/share/gnome-background-properties/mojave.xml && 
chmod 644 /usr/share/gnome-background-properties/mojave.xml
```
