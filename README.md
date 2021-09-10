## 基于DHDAXCW骷髅头的R2S固件（docker版本）进行修改
# 目前主要改动如下
1. 将全能推送（luci-app-pushbot）替换为原微信推送（luci-app-serverchan）
2. 恢复加入Onliner User（luci-app-onliner）Watchcat（luci-app-watchcat）
3. 将ROOTFS_PARTSIZE翻倍适当缩小，加快编译（需要扩容请使用diskgenius（适用sq固件）或gparted（适用ext4固件））
4. 加入编译优化选项CONFIG_TARGET_OPTIMIZATION="-O3 -pipe -march=armv8-a+crypto+crc -mcpu=cortex-a53+crypto+crc -mtune=cortex-a53"（虽然modify_config.sh好像已经做了这件事...）
