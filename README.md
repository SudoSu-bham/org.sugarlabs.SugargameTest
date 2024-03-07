# Sugargame Activity Flatpak

Sugargame is a Python package which allows Pygame programs to run well under Sugar. It is fork of olcpgames, which is no longer maintained.  
It has a `TestGame.py` in `test/` directory which is a sugar activity, it is a bouncing ball game which you can run in flatpak.  
To know more refer: https://github.com/sugarlabs/sugargame

## How to build

To build this run the following command in terminal

Install the latest version of BaseApp  

```bash
flatpak -y --user install org.sugarlabs.BaseApp
```

```bash
https://github.com/SudoSu-bham/org.sugarlabs.SugargameTest.git
cd org.sugarlabs.SugargameTest
flatpak -y --user install org.gnome.{Platform,Sdk}//44
flatpak-builder --user --force-clean --install build org.sugarlabs.SugargameTest.json
```


## Check for updates
Install the flatpak external data checker

```bash
flatpak --user install org.flathub.flatpak-external-data-checker
```
To update every Single module to the latest stable version use

```bash
cd org.sugarlabs.SugargameTest
flatpak run --filesystem=$PWD org.flathub.flatpak-external-data-checker org.sugarlabs.SugargameTest.json
```
