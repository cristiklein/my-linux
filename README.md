# My Linux

This is how I compile Linux for my Lenovo ThinkPad X1 Carbon Gen 12.

```shell
git clone \
    --branch linux-6.13.y \
    --depth 1 \
    https://git.kernel.org/pub/scm/linux/kernel/git/stable/linux.git
cd linux
cp ../config-6.13.3 .config
time KBUILD_BUILD_TIMESTAMP='' make CC="ccache gcc" -j$(nproc) deb-pkg
```
