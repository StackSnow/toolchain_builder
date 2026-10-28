# toolchain_builder

A CMake project that builds bundled C/C++ libraries as static libraries.

The top-level build currently includes:

- zlib
- JPEG
- libpng
- libtiff
- FreeType

The repository also contains GLFW sources, OpenGL headers, and a GLFW test
program. These are not added to the top-level CMake build.

## Build

Requirements: CMake 3.10 or later and a C/C++ compiler toolchain.

```powershell
cmake -S . -B build
cmake --build build --config Release
```

The `USE_WASM_OPTIONS` CMake cache variable controls the WebAssembly build
flags. It defaults to `1`; set it to `0` to disable those flags or `2` to
enable the `MEMORY64` option.

## License

Project-specific files are licensed under the MIT License in `LICENSE`.
Bundled third-party components retain their own copyright notices and license
terms; see the notices in their respective directories before using or
redistributing them.
