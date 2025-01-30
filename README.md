# hello-yocto-recipe

A simple C program with multiple build system generators (CMake, Autoconf & Meson)
to be used as a test/exmaple recipe in the Yocto project

# Artifacts
`yocto-recipe` program

## Add the recipe to Yocto
```shell
devtool add https://github.com/amahran/hello-yocto-recipe
```

## Edit the recipe
```shell
devtool edit-recipe hello-yocto-recipe
```
For example you can switch the build system from CMake to Autotools or meson

## Bake the recipe
```shell
bitbake hello-yocto-recipe
```

## Add the recipe to an image
Then you can add the recipe to an image (e.g. `core-image-minimal`) and rebuild
your image
```shell
bitbake core-image-minimal
```

## Test the recipe artifacts
After booting into your target (e.g. beaglebone), you can run the recipe using:
```shell
yocto-recipe
```
