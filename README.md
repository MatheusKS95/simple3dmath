# Matheus' Simple 3D Math
Extremely basic 3D math library for OpenGL and related APIs/libraries/etc.
I made this for a game/game engine that "failed", but this math code works so why not share it here?

As far as testing goes, it worked with OpenGL and sokol-gfx. Not tested with other stuff (such as Vulkan or wgpu-native).

## What this does
Math stuff needed for 3D rendering such as vectors, matrices, quaternions...

## What this does not
This is way smaller than CGLM and linmath.h. Probably doesn't do very advanced stuff that you might need.

It also doesn't implement SIMD neither similar optimizations.

Use at your own risk.

## How to use
You can simply copy-paste the header and implementation file into your project, and it's ready to use. No need for awkward build systems like CMake or Premake and also no need for stuff like ```#define SOMETHING_IMPLEMENTATION``` like header-only libraries often require.

If you want to compile and use it as a shared library you can simply do (on any system with GCC):

```
gcc -c -Wall -Werror -fpic 3d_math.c -o 3d_math.o && gcc -shared -o lib3dmath.so 3d_math.o
```
Or as a static library (also using GNU stuff):

```
gcc -c -Wall -Werror 3d_math.c -o 3d_math.o && ar rcs lib3dmath.a 3d_math.o
```

## License
I'm sharing this code under the Mozilla Public License 2.0

It offers better protection than most permissive licenses, but this library is not complex enough to warrant the GPL in my opinion. MPL also doesn't have the overcomplicated linking requirements like LGPL, so you can use it on any software, proprietary or open source, as long as you comply with the MPL. Check ```LICENSE``` file for more details.
