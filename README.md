# Ventoy Optimized

![Ventoy Version](https://img.shields.io/badge/Ventoy-1.0.99+-blue)
![License](https://img.shields.io/badge/License-MIT-green)
![Status](https://img.shields.io/badge/Status-Stable-brightgreen)
![Compatibility](https://img.shields.io/badge/OS-Windows%20%7C%20Linux-lightgrey)

The Ventoy boot disk configuration file collection includes:

- Custom GRUB boot entries (VMD/NVIDIA/ASPM disabled)
- BIOS optimization settings logs
- Multiple boot configurations for Fedora/Ubuntu

---

## Table of Contents

- [Supported ISO Versions](#supported-iso-versions)
- [Important Notices](#important-notices)
- [`ventoy.json` Example](#ventoy-json)
- [Reference](#reference)
- [Metadata & License](#metadata-license)

---

## Supported ISO Versions <a id="supported-iso-versions"></a>

The current `.cfg` files have been tested and work for the following ISO versions:

| Configuration | Fedora | Ubuntu |
| :--- | :--- | :--- |
| `vmd-off.cfg` | 43, 44 | 22.04.5, 24.04.4 |
| `vmd-nvidia-off.cfg` | 43, 44 | 22.04.5, 24.04.4 |
| `vmd-nvidia-aspm-off.cfg` | 43, 44 | 22.04.5, 24.04.4 |

> **Note**: Other versions may require modification of the ISO filename and `CDLABEL` parameters.

---

## Important Notices <a id="important-notices"></a>

> [!CAUTION]
> `ventoy.json` and `ventoy_grub.cfg` must be in **UTF-8** encoding.

> [!ATTENTION]
> Use `WIMBOOT mode` only when you run into problem with the default mode.
> `WIMBOOT` can only be used to boot official Windows ISO files and some WinPE ISO files.

> [!ATTENTION]
> Use `GRUB2 mode` only when you run into problem with the default mode.
> `GRUB2 mode` can only be used to boot Linux ISO which contains grub2 configuration file and can not be used to boot `Windows/WinPE/Unix` ...

---

## `ventoy.json` Example <a id="ventoy-json"></a>

```json
{
    "control": [
        { "VTOY_DEFAULT_MENU_MODE": "1" },
        { "VTOY_FILT_DOT_UNDERSCORE_FILE": "1" }
    ],

    "theme": {
        "file": "/ventoy/theme/blur/theme.txt",
        "gfxmode": "1920x1080"
    },

    "auto_install" : [
        {
            "image": "/ISO/cn_windows_server_2012_r2_vl_x64_dvd_2979220.iso",
            "template": "/ventoy/script/windows_unattended.xml"
        },
        {
            "image": "/000/centos.iso",
            "template": "/ventoy/script/centos_kickstart.cfg"
        }
    ]
}
```

To see more details, you can visit [VentoyPlugson](https://www.ventoy.net/en/plugin_entry.html)

---

## Reference <a id="reference"></a>

- [Ventoy Global Control Plugin](https://www.ventoy.net/en/plugin_control.html)
- [VentoyPlugson](https://www.ventoy.net/en/plugin_plugson.html)
- [Fedora Linux](https://fedoraproject.org/)
- [Ubuntu](https://ubuntu.com/download)

---

## Metadata & License <a id="metadata-license"></a>

- **Author**：[@autentisitet](https://github.com/autentisitet)
- **Version**：v1.0
- **License**：[MIT](LICENSE)
