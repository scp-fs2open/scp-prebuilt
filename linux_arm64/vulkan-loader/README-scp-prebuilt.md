Built from vulkan-sdk-1.4.341 branch of Vulkan-Loader in Ubuntu 20.04 container.

```
git clone https://github.com/KhronosGroup/Vulkan-Loader
cd Vulkan-Loader
git checkout vulkan-sdk-1.4.341
mkdir build
cd build
cmake .. -GNinja -DCMAKE_BUILD_TYPE=MinSizeRel -DUPDATE_DEPS=ON
ninja
strip loader/libvulkan.so.1.4.341
```
