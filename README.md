# clang-build


This is a CMake project to easily download and compile llvm + clang + extra
tools (also with include-what-you-use).


## How to use

First, clone this repo and descend to it:

```bash
git clone https://github.com/biojppm/clang-build
cd clang-build   # following commands assume we're inside this folder
```

The examples below use [cmany](https://github.com/biojppm/cmany).

Compile clang 7.0.1 (the default):

```bash
# using cmany:
cmany b

# ... or equivalently using CMake:
mkdir build
cmake -H . -B build -D CMAKE_BUILD_TYPE=Release
cmake --build build

```

That's it! llvm and clang 7.0.1 are automatically downloaded and compiled.
If you have a different version in mind, say 6.0.1, use the CMake project
variable `CLANG_VERSION`:

```bash
# using cmany:
cmany b -V CLANG_VERSION=6.0.1

# ... or equivalently using CMake:
mkdir build
cmake -H . -B build -D CMAKE_BUILD_TYPE=Release -D CLANG_VERSION=7.0.1
cmake --build build
```


## License

Permissively licensed with the [MIT license](LICENSE.txt).

