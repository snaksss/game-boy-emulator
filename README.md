# Game Boy Emulator

A beginner-friendly project to build a Game Boy emulator from scratch using C and SDL2. This project will simulate the hardware of the Game Boy and allow us to load and play simple ROMs like Tetris.

## Features
- Emulate the Game Boy CPU (instructions, registers, memory).
- Load and run Game Boy ROMs.
- Render graphics on the screen.
- Handle basic input (keyboard mapped to Game Boy buttons).

## Roadmap
### Milestone 1: Project Setup
- [x] Set up project folder structure.
- [x] Install SDL2 on macOS and Windows.
- [ ] Write a basic SDL2 program to open a window.
- [ ] Add `README.md` and `BUILD.md` files to the repository.

### Milestone 2: Emulator Skeleton
- Define memory map.
- Implement CPU registers.
- Create a fetch-decode-execute loop.

### Milestone 3: ROM Loading
- Write a function to load Game Boy ROMs into memory.
- Log ROM data for debugging.