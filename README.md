# Meson build for Rang (a lightweight C++ header only lib for colorful terminal output)

URL: 

- [Github: rang](https://github.com/agauniyal/rang);
- [Github: meson-cxxopts (this project)](https://github.com/randydu/meson-rang);
- [The Meson Build system](https://mesonbuild.com/index.html);

The subfolder "src" is a clone of git repository of a specified release version. 
unit-tests are not built as part of the meson-build.

## Versions

The "revision" of cxxopts.wrap and the version of this meson-build project matches the embedded submodule cxxopts version as following:

meson-rang |  rang 
------------|-----------
1.0         | v3.2


## Usage

copy rang.wrap to "subprojects" sub-folder of your main project directory.


in meson.build:

```
# import

rang_dep = dependency('rang')

# use
srcs = ['main.cpp', ...]

executable('test', srcs, dependencies: [rang_dep, ...])

```

in main.cpp:

```cpp
#include <rang.hpp>

using namespace rang;

int main(int argc, char* argv[]){
  std::cout << style::bold << "Hello World!" << style::reset << std::endl;
  ...
}
```



