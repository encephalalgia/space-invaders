# 👾 Space Invaders 👾
This is an emulator of the 1978 Taito arcade machine [Space Invaders](https://en.wikipedia.org/wiki/Space_Invaders) running on top of my [Intel8080 emulator](https://github.com/amelliyaa/intel8080). It comes with color, sound, and high score persistence!
<p align="center">
  <img alt="Spacefight Invaders attract mode gif" src="https://raw.githubusercontent.com/amelliyaa/space-invaders/master/examples/attract_mode.gif" height="400" />
</p>

# Controls
| Key         | Action                            |
|-------------|-----------------------------------|
| C           | deposit credits                   |
| 1           | start the game in one-player mode |
| 2           | start the game in two-player mode |
| left arrow  | move left                         |
| right arrow | move right                        |
| space       | shoot                             |
| T           | tilt the machine                  |

# Usage
### Dependencies
* **A c++ compiler**
* **CMake version 3.26+**
* **CMake build generator**
* **[SDL2](https://github.com/libsdl-org/SDL)**
* **[SDL_mixer](https://github.com/libsdl-org/SDL_mixer)**

### Build & Run
1) Download the source code
    ```
    git clone https://github.com/amelliyaa/space-invaders.git
    cd space-invaders
    ```
2) **Optional:** If you want, you can customize the colors of the emulator by changing the color code constants defined in [Display.h](src/components/Display.h).  
3) Build
   ```
   cmake -S . -B build -G <generator> -DCMAKE_BUILD_TYPE=RELEASE -DCMAKE_PREFIX_PATH=<path/to/sdl>
   cmake --build build --config Release
   ```
4) Add the [ROMs](assets/roms) and [sound files](assets/sound) to the assets folder.
5) Run the executable
   ```
   build/src/space-invaders.exe <PARAMETERS...>
   ```
   
### DIP Switch
Replace `<PARAMETERS...>` with zero or more of the following:

| Parameter         | Range        | Default | Description                                               |
|-------------------|--------------|---------|-----------------------------------------------------------|
| `-lives <n>`      | [3,6]        | 3       | changes the number of lives you start with                |
| `-extra_life <n>` | 1500 or 1000 | 1500    | changes the amount of points needed to gain an extra life |

# Resources
[Computer Archeology Space Invaders](https://computerarcheology.com/Arcade/SpaceInvaders/)
