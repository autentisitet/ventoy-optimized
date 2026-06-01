# Pitfalls dualsystem(Chinese Content)

## Day 1

- ​电脑默认开启`VMD`，无法`GRUB CLI`写`.cfg`绕过，需要进 BIOS 隐藏菜单关闭(否则装不了Fedora)

- ​Fedora44太新，diskgenius、ventoy识别不出iso内部linux文件类型( → 降级选择旧版本)

- ​Nvidia独显架构不适配，在linux引导时就接管图形栈，linux不会自动退回使用Intel核显，导致进不去linux界面( → 禁用Nvidia独显)

- 长按物理关机键关不了机( → 拔掉电源适配器充电线再按几秒就成功了)

---

## Day 2

- `VMD`关闭后，由于注册表`HKLM`里面的一些kv配置，导致`Windows boot manager`引导时立即调用`VMD`驱动，进不去Windows，后面被我自己改了注册表kv，但是数据库乱了( → 只好重装Windows系统盘)

​- 备份`Linux GRUB`、`Windows BCD`
