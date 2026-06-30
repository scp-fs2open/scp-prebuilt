Built from vulkan-sdk-1.4.341 branch of Vulkan-Loader

```
git clone https://github.com/KhronosGroup/Vulkan-Loader
cd Vulkan-Loader
git checkout vulkan-sdk-1.4.341
mkdir build
cd build
cmake .. -GNinja -DCMAKE_BUILD_TYPE=MinSizeRel -DCMAKE_C_FLAGS="/DNTDDI_VERSION=NTDDI_VISTA /D_WIN32_WINNT=_WIN32_WINNT_VISTA" -DUPDATE_DEPS=ON
```

> [!TIP]
> If building for win32 or x64 on an ARM64 system add these flags to the CMake
> configuration to allow proper building with their quirky CMake setup:
> `-DCMAKE_SYSTEM_NAME=Windows -DCMAKE_SYSTEM_PROCESSOR=AMD64`
