# ubuntu-configs
My Ubuntu configurations and scripts.

# Instalação de Apps
### Davinci Resolve
```
sudo apt install distrobox
```
```
distrobox-create --name Davinci-Fedora-37 --image fedora:37
```
```
sudo dnf install alsa-plugins-pulseaudio libxcrypt-compat xcb-util-renderutil xcb-util-wm pulseaudio-libs xcb-util xcb-util-image xcb-util-keysyms libxkbcommon-x11 libXrandr libXtst mesa-libGLU mtdev libSM libXcursor libXi libXinerama libxkbcommon libglvnd-egl libglvnd-glx libglvnd-opengl libICE librsvg2 libSM libX11 libXcursor libXext libXfixes libXi libXinerama libxkbcommon libxkbcommon-x11 libXrandr libXrender libXtst libXxf86vm mesa-libGLU mtdev pulseaudio-libs xcb-util alsa-lib apr apr-util fontconfig freetype libglvnd fuse-libs
```
AMD GPU:
```
sudo dnf install rocm-openCL
```
NVIDIA GPU (with RPM Fusion):
```
sudo dnf install akmod-nvidia  xorg-x11-drv-nvidia-cuda
```
```
echo $DISPLAY
```
O resultado deve ser algo como :0 ou :0.0.
```
sudo dnf install xhost-[TAB]
```
```
xhost +local:docker
```
```
distrobox-enter --display=$DISPLAY
```
```
sudo ./DaVinci_Resolve_[TAB]
```
