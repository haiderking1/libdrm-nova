# libdrm-nova, haider's libdrm fork

libdrm with one change for my [nova](https://github.com/haiderking1/nova)
stack: DRM devices on the auxiliary bus, such as nova-drm (the DRM driver of
nova, the Rust NVIDIA kernel driver), are described by their PCI parent
(`xf86drm: describe DRM devices on the auxiliary bus by their parent`).
Without it `drmGetDevices2()` skips them, and Mesa's NVK finds no GPU.

For libdrm itself, see `README.rst`. Branch: `soka/nova`.
