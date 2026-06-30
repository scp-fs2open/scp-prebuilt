Built from "known-good" config for Shaderc v2026.1 in Ubuntu 20.04 container.

```
git clone https://github.com/google/shaderc
cd shaderc
git checkout known-good
./update_shaderc_sources.py
cd src
mkdir build
cd build
cmake .. -GNinja -DCMAKE_BUILD_TYPE=MinSizeRel
ninja shaderc_shared
strip libshaderc/libshaderc_shared.so.1
```

