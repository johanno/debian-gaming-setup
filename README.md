# debian-gaming-setup
A list of Todos to get steam and discord running on Debian.

1. add non-free ona contrib to sources.list:

deb http://deb.debian.org/debian/ testing main non-free contrib
deb-src http://deb.debian.org/debian/ testing main non-free contrib

deb http://security.debian.org/debian-security testing/updates main contrib non-free
deb-src http://security.debian.org/debian-security testing/updates main contrib non-free

2. sudo dpkg --add-architecture i386

3. sudo apt update

4. sudo apt install steam-installer

5. NVIDIA:
   sudo apt install nvidia-driver // if not already done
   sudo apt install nvidia-driver-libs:i386

6. optional:
   sudo apt install libgtk2.0-0:i386
   sudo apt install mesa-vulkan-drivers libglx-mesa0:i386 mesa-vulkan-drivers:i386 libgl1-mesa-dri:i386


DISCORD:
https://flatpak.org/setup/Kubuntu
https://flatpak.org/setup/Debian

1. sudo apt install flatpak

2. flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo

3. install flatpak plugin under discover:
   sudo apt install plasma-discover-backend-flatpak
