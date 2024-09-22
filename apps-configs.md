# Configuração de Apps
### Davinci Resolve [(Source)](https://www.youtube.com/watch?v=wmRiZQ9IZfc)
``` bash
sudo apt install distrobox
```
``` bash
distrobox-create --name Davinci-Fedora-37 --image fedora:37
```
``` bash
distrobox enter Davinci-Fedora-37
```
``` bash
sudo dnf install alsa-plugins-pulseaudio libxcrypt-compat xcb-util-renderutil xcb-util-wm pulseaudio-libs xcb-util xcb-util-image xcb-util-keysyms libxkbcommon-x11 libXrandr libXtst mesa-libGLU mtdev libSM libXcursor libXi libXinerama libxkbcommon libglvnd-egl libglvnd-glx libglvnd-opengl libICE librsvg2 libSM libX11 libXcursor libXext libXfixes libXi libXinerama libxkbcommon libxkbcommon-x11 libXrandr libXrender libXtst libXxf86vm mesa-libGLU mtdev pulseaudio-libs xcb-util alsa-lib apr apr-util fontconfig freetype libglvnd fuse-libs
```
AMD GPU:
``` bash
sudo dnf install rocm-openCL
```
NVIDIA GPU (with RPM Fusion):
``` bash
sudo dnf install akmod-nvidia xorg-x11-drv-nvidia-cuda
```
``` bash
sudo ./DaVinci_Resolve_[TAB]
```
Solução para "qt.qpa.xcb: could not connect to display"
``` bash
echo $DISPLAY
```
O resultado deve ser algo como :0 ou :0.0.
``` bash
sudo dnf install xhost-[TAB]
```
``` bash
xhost +local:docker
```
``` bash
distrobox-enter --display=$DISPLAY
```
``` bash
sudo ./DaVinci_Resolve_[TAB]
```
Solução para "Unsupported GPU Processing Mode" [(Source)](https://nobaraproject.org/docs/davinci-resolve/configuring-davinci-resolve-with-amd-gpus/)
``` bash
sudo dnf install mesa-libOpenCL apr apr-util
```
Alias (bash)
``` bash
echo 'alias davinci="distrobox enter Resolve-Fedora-37 -- /opt/resolve/bin/resolve; -- exit"' >> ~/.bash_aliases; source ~/.bashrc
```
```
davinci
```
