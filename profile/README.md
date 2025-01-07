## vitasdk — softfp fork
This organization provides softfp version of [VitaSDK](https://vitasdk.org), it's package manager, and packages. Softfp is useful for Android->Vita ports done via so-loader.

One difference from upstream `packages` is that instead of standard SDL2, [Northfear's SDL2-vitagl](https://github.com/Northfear/SDL) fork is provided by default.
This fork makes use of VitaGL as rendering backend instead of standard GXM and thus allows managing GL context through SDL (using SDL_GL stuff) unlike the upstream version.

**Last fork synchronization with upstream:** Apr 26 2024.

## How to install

Follow instructions on [https://vitasdk.org/](https://vitasdk.org) BUT replace the organization in `git clone https://github.com/vitasdk/vdpm` command with `vitasdk-softfp`, like so:
```bash
git clone https://github.com/vitasdk-softfp/vdpm
cd vdpm
<... other commands ...>
```

Make sure that you delete or rename your old $VITASDK (if you had one) to avoid any potential conflicts. Hardfp (standard) and softfp SDK can exist alongside each other without any issue
as long as you keep them in separate directories (e.g. `/usr/local/vitasdk-softp` && `/usr/local/vitasdk-hardfp` and adjust `$VITASDK` environment variable when needed).
