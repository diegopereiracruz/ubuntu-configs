# XFCE
### Systray icons desapearing [(Source)](https://forum.xfce.org/viewtopic.php?id=17218)
``` bash
apt list --installed | grep ayatana-indicator-application
```
``` bash
sudo apt remove ayatana-indicator-application
```
``` bash
xfce4-panel -r
```
``` bash
xfce4-panel &
```
