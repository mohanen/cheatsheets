# Development - C, C++, Cuda

## IDE

### Qt Creator

- c, c++, python, and qt stuffs
- Written in **Qt**
- **Light Weight**

### vs-code & atom

- **Text editor** extended with extensions
- **Resource intensive**
- Written in **Electron**, basically a browser

### sublime text

- **Text editor** with IDE features
- Written in **c++ & python**
- **Light Weight**

### clion

- **Intellij's** Robust c, c++ target IDE
- Written in **Java**
- **Resource intensive**

> There are more, but only considering the actively developed and popular ones

## Compilers Steps

**Front-end** $->$ IR $->$ **Optimizations** $->$ IR $->$ **Code Generation**

### IR

- **Intermediate representation**, a standard meant to keep the compiler modular
- A compiler can convert different language source files to the same IR so the next step can be general.

### Front-end

- Understands the source language and converts it into a common (for the compiler) intermediate representation.

### Optimizations

- A bunch of machine independent optimizations are performed on the IR.

### Code Generation

- Target (machine) specific optimizations are performed and code/assembly is generated.

## Compilers

### GCC

- Developed by **GNU**
- **commonly used** compiler for linux.

### LLVM

- LLVM (**Low Level Virtual Machine**) developed by **Chris Lattner** in **2000** later used by **Apple**.
- Uses **GCC as Front-end**
- Optimizes program languages and links during compilation, runtime, and idle time and generate code

### Clang

- Apple's LLVM is still limited by GCC's features, so **Apple created Clang** from scratch in **2007**
- Clang replaced GCC in GCC + LLVM
- Provides **performance superior** to GCC

## Build Systems

### make

- Build automation tool that automatically builds executable programs and libraries from source code by reading files called Makefiles

### ninja

- Small build system with a **focus on speed**.
- Meant to **replace Make**, which is slow when performing incremental (or no-op) builds
- Ninja build files are not meant to be written by hand.

> There are other platform dependent systems also exist.

## Build generators

### cmake

- Cross-platform, FOSS
- Great support for multiple backends (Make, Qt Creator, Ninja, Apple's Xcode, and Microsoft Visual Studio).
- The **scripting language is cumbersome** to work with.
- Some simple things are more complicated than necessary.

### meson

- FOSS written in **Python**
- Supports GNU Compiler Collection, Clang, Microsoft Visual Studio and others.
- The **fastest build system**, **user friendly**, designed to be as invisible to the developer as possible, native support for modern tools (precompiled headers, coverage, Valgrind etc).
- Not Turing complete so **build definition files are easy to read and understand**.
- **Relatively new** so less community support.

### GNU Autotools

- Excellent support for legacy Unix platforms, large selection of existing modules.
- Needlessly slow, complicated, hard to use correctly, unreliable, painful to debug, incomprehensible for most people, poor support for non-Unix platforms (especially Windows).

### SCons

- Full power of Python available for defining your build.
- Slow.
- Requires you to pass your configuration settings on every invocation while every other build system remembers build options from the previous invocation.

### Bazel

- Developed by: Google
- Proven to scale to very large projects.
- Implemented in Java.
- Poor Windows support.
- Heavily focused on Google's way of doing things (which may be a good or a bad thing). Contributing code requires signing a CLA.
