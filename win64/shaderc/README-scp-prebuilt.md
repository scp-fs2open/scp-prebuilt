Built from "known-good" config for Shaderc v2026.1.

```
git clone https://github.com/google/shaderc
cd shaderc
git checkout known-good
./update_shaderc_sources.py
cd src
mkdir build
cd build
cmake .. -GNinja -DCMAKE_BUILD_TYPE=MinSizeRel -DCMAKE_C_FLAGS="/DNTDDI_VERSION=NTDDI_VISTA /D_WIN32_WINNT=_WIN32_WINNT_VISTA" -DCMAKE_CXX_FLAGS="/DNTDDI_VERSION=NTDDI_VISTA /D_WIN32_WINNT=_WIN32_WINNT_VISTA"
ninja shaderc_shared
```
Built from "known-good" config for Shaderc v2026.1.

```
git clone https://github.com/google/shaderc
cd shaderc
git checkout known-good
./update_shaderc_sources.py
cd src
mkdir build
cd build
cmake .. -GNinja -DCMAKE_BUILD_TYPE=MinSizeRel -DCMAKE_C_FLAGS="/DNTDDI_VERSION=NTDDI_VISTA /D_WIN32_WINNT=_WIN32_WINNT_VISTA" -DCMAKE_CXX_FLAGS="/DNTDDI_VERSION=NTDDI_VISTA /D_WIN32_WINNT=_WIN32_WINNT_VISTA"
ninja shaderc_shared
```
