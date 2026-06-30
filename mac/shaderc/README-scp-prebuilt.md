Built from "known-good" config for Shaderc v2026.1.

```
git clone https://github.com/google/shaderc
cd shaderc
git checkout known-good
./update_shaderc_sources.py
cd src
mkdir build
cd build
cmake .. -GNinja -DCMAKE_BUILD_TYPE=MinSizeRel -DCMAKE_OSX_ARCHITECTURES="x86_64;arm64" -DCMAKE_OSX_DEPLOYMENT_TARGET="11.0"
ninja shaderc_shared
strip -x -S libshaderc/libshaderc_shared.1.dylib
codesign --force --timestamp --deep --sign - libshaderc/libshaderc_shared.1.dylib
```
