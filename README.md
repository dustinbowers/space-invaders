# Intel 8080 Emulator (for Space Invaders)

An Intel 8080 emulator using SDL, meant for running Space Invaders by Taito.

![Build Status](https://github.com/dustinbowers/intel8080emu/actions/workflows/build.yml/badge.svg)

## Gameplay 

<img src="https://github.com/dustinbowers/intel8080emu/blob/master/screens/gameplay.gif" width="40%">

## Input

| Key     	| Description              	|
|---------	|--------------------------	|
|    C    	| Insert coin              	|
| [Space] 	| P1 Start                 	|
|   A/D   	| P1 move Left/Right       	|
|    W    	| P1 shoot                 	|
|    T    	| Tilt machine (Game Over) 	|



## Requirements:

Install necessary dependencies:

**Mac:** `brew install sdl2{,_image,_mixer,_ttf,_gfx} pkg-config`

**Linux:** `sudo apt install -y libsdl2{,-image,-mixer,-ttf,-gfx}-dev`

## Build / Run

Build with `make` (you may need to modify the Makefile to build for your particular OS).  
The binary by default looks for a `.roms/` directory beside it. This directory must contain the files referenced in `main.go` 

## Testing

```
./build/space-invaders-darwin -test=roms/tests/TST8080.COM
Launching...
Running a test ROM - roms/tests/TST8080.COM
loading roms/tests/TST8080.COM
1792 bytes loaded
MICROCOSM ASSOCIATES 8080/8085 CPU DIAGNOSTIC
 VERSION 1.0  (C) 1980

 CPU IS OPERATIONAL
 ```

## TODO
- [ ] Add sound
- [ ] Add player 2 support

## Resources
https://pastraiser.com//cpu/i8080/i8080_opcodes.html

http://www.classiccmp.org/dunfield/r/8080.txt

http://www.nj7p.org/Manuals/PDFs/Intel/9800301C.pdf

http://kazojc.com/elementy_czynne/IC/INTEL-8080A.pdf
