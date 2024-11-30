
---

#### **BUILD.md**

```markdown
# Building the Game Boy Emulator

This guide will help you set up the emulator on macOS and Windows.

---

## macOS
1. **Install SDL2**:
   - Open your terminal and run:
     ```bash
     brew install sdl2
     ```

2. **Compile the program**:
   - Navigate to the project folder in your terminal.
   - Compile the `main.c` file:
     ```bash
     gcc -o build/emulator src/main.c -lSDL2
     ```
   - Run the emulator:
     ```bash
     ./build/emulator
     ```

---

## Windows
1. **Install SDL2**:
   - Download the SDL2 development library from [https://libsdl.org](https://libsdl.org).
   - Extract the files and follow the instructions for your compiler (e.g., MinGW or Visual Studio).

2. **Compile the program**:
   - Open a terminal or your IDE and compile `src/main.c`.
   - If using MinGW, use this command:
     ```bash
     gcc -o build/emulator src/main.c -lmingw32 -lSDL2main -lSDL2
     ```
   - Run the program:
     ```bash
     emulator.exe
     ```

---

## Notes
- **Dependencies**: SDL2 is required to compile and run the program.
- Make sure your system PATH is set up correctly for your compiler.