# clang-build

This is a CMake project to easily download and compile llvm + clang + extra
tools, also with include-what-you-use.

Example using [https://github.com/biojppm/cmany](cmany):

```bash
git clone https://github.com/biojppm/clang-build
cd clang-build
cmany b -V CLANG_VERSION=7.0.1  # compile clang 7.0.1
```

or using cmake (same effects):

```bash
git clone https://github.com/biojppm/clang-build
cd clang-build
mkdir build
cmake -H . -B build \
    -D CMAKE_BUILD_TYPE=Release \
    -D CLANG_VERSION=7.0.1   # compile clang 7.0.1
cmake --build build
```

## License

Permissively licensed with the [./LICENSE.txt](MIT license).

