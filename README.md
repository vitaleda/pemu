# pemu

**Building - Windows => Windows (x64)**
- download, install and update [MYSYS2](http://www.msys2.org/)
- install dependencies:  
	- `pacman -S git zip automake autoconf make mingw-w64-x86_64-gcc mingw-w64-x86_64-SDL2 mingw-w64-x86_64-freetype mingw-w64-x86_64-cmake mingw-w64-x86_64-glm mingw-w64-x86_64-glew mingw-w64-x86_64-libconfig mingw-w64-x86_64-json-c mingw-w64-x86_64-zlib`
- clone pemu repository:
	- `git clone --recursive https://github.com/Cpasjuste/pemu.git`
- build:
	- `mkdir cmake-build && cd cmake-build`
	- `cmake ../ -G "MSYS Makefiles" -DBUILD_WINDOWS=ON -DCMAKE_BUILD_TYPE=Release`

**Building - Ubuntu => Nintendo Switch**
- install ubuntu build tools:
	- `sudo apt-get install git autoconf libtool automake build-essential cmake`
- download, install and update devkitpro-pacman:
	- `wget https://github.com/devkitPro/pacman/releases/download/devkitpro-pacman-1.0.1/devkitpro-pacman.deb && sudo dpkg -i devkitpro-pacman.deb`
	- `sudo dkp-pacman -Syu`
	- `sudo dkp-pacman -S switch-dev switch-bulletphysics switch-bzip2 switch-curl switch-flac switch-freetype switch-giflib switch-glad switch-glfw switch-glm switch-jansson switch-libass switch-libconfig switch-libdrm_nouveau switch-libexpat switch-libfribidi switch-libjpeg-turbo switch-libjson-c switch-liblzma switch-liblzo2 switch-libmad switch-libmikmod switch-libmodplug switch-libogg switch-libopus switch-libpcre2 switch-libpng switch-libsamplerate switch-libtheora switch-libtimidity switch-libvorbis switch-libvorbisidec switch-libxml2 switch-mbedtls switch-mesa switch-mpg123 switch-ode switch-opusfile switch-pkg-config switch-sdl2 switch-sdl2_gfx switch-sdl2_image switch-sdl2_mixer switch-sdl2_net switch-sdl2_ttf switch-zlib switch-zziplib devkitpro-pkgbuild-helpers`
- clone pemu repository:
	- `git clone --recursive https://github.com/Cpasjuste/pemu.git`
- build:
	- `mkdir cmake-build && cd cmake-build`
	- `cmake ../ -DBUILD_SWITCH=ON -DCMAKE_BUILD_TYPE=Release`
	
