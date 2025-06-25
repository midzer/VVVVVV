# Emscripten

## Build

```
cd desktop_version
mkdir build
cd build
emcmake cmake ..
emmake make
```

## Link

```
em++ -flto -O3 -fno-rtti -fno-exceptions *.o ../../../libc-hashmap-static.a ../../../libfaudio-static.a ../../../libInterimVersion.a ../../../liblodepng-static.a ../../../libphysfs-static.a ../../../libsheenbidi-static.a ../../../libtinyxml2-static.a -o index.html -sUSE_SDL=2 -sTOTAL_MEMORY=312mb -sENVIRONMENT=web --preload-file data.zip --closure 1 -sEXPORTED_RUNTIME_METHODS=['allocate','ALLOC_NORMAL']
```
