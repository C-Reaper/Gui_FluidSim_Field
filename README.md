## Project README

### Overview
This project is a simple fluid simulation that visualizes flow fields using a graphical user interface. It demonstrates the implementation of fluid dynamics in C and showcases cross-platform development using various build systems.

### Features
- Fluid simulation
- Real-time visualization of flow field using a pixel buffer
- Cross-platform support: Linux, Windows, Wine, and WebAssembly

### Project Structure
```
Project/
├── build/              # .exe files produced by Main.c
├── libs/               # *.c for bin (not present in this project)
├── src/                # Source code directory
│   ├── Main.c          # Entry point of the application
│   └── *.h             # Standalone header-based C-files
├── Makefile.linux      # Linux Build configuration
├── Makefile.windows    # Windows Build configuration
├── Makefile.wine       # Wine Build configuration
├── Makefile.web        # Emscripten Build configuration
└── README.md           # This file
└── LICENSE             # License information
└── .gitignore          # Ignore files for git
```

## Prerequisites
- C/C++ Compiler and Debugger (GCC, Clang)
- Make utility
- Standard development tools
- Libraries needed in specific projects:
  - Linux: X11 for GUI, PNG/JPEG for image handling
  - Windows: User32, GDI32, Winmm (for Windows API functions)

## Build & Run

### Build Process
To build the project, navigate to the project directory and run:

```bash
make -f Makefile.(os) all
```

Replace `(os)` with `linux`, `windows`, `wine`, or `web` depending on your target platform.

#### Clean Rebuild
For a clean rebuild, use:

```bash
make -f Makefile.(os) clean
make -f Makefile.(os) all
```

#### Build Options
- `make -f Makefile.(os) all`: Builds the output executable.
- `make -f Makefile.(os) do`: Builds and runs the executable.
- `make -f Makefile.(os) clean`: Removes build artifacts.

### Execute

To execute the built application, use:

```bash
make -f Makefile.(os) exe
```

This will run the compiled binary using the appropriate command for your operating system.