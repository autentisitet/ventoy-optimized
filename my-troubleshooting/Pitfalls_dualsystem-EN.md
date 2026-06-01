# Pitfalls dualsystem(English Content)

## Day 1

- VMD is enabled by default on the computer, making it impossible to bypass the GRUB CLI by writing cfg. It needs to be disabled in the BIOS hidden menu (otherwise Fedora cannot be installed).

- Fedora 44 is too new; DiskGenius and Ventoy cannot recognize the Linux file type inside the ISO ( → downgrade to an older version).

- The Nvidia discrete graphics card architecture is incompatible; it takes over the graphics stack during Linux boot, preventing Linux from automatically reverting to the Intel integrated graphics, thus preventing access to the Linux interface ( → disable the Nvidia discrete graphics card).

- Holding down the physical power button fails to shut down the computer ( → unplugging the power adapter and then pressing the button again for a few seconds resolves the issue).

---

## Day 2

- After disabling VMD, some key-value (KV) configurations in the HKLM registry caused Windows Boot Manager to immediately call the VMD driver during boot, preventing access to Windows. I later modified the registry KV, but the database became corrupted ( → I had to reinstall the Windows system disk).

- Back up Linux GRUB and Windows BCD.

---
