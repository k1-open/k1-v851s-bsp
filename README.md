# K1 V851S BSP

K1 外挂式智能眼镜的 V851S 板级支持资料，用于管理 Tina SDK 的板级配置、设备树、分区、启动参数和非显示驱动适配。

## 1. 当前内容

- `vendor/v851s-tina/device/config/chips/v851s/configs/`：板级候选配置
- `docs/guides/`：主板下载、OTA 升级和调试说明
- `docs/vendor/v851s-tina/`：Allwinner V851S/Tina 平台参考资料
- `tools/`：PhoenixSuit 和 USB 烧录驱动

`perf1` 是与 K1 硬件最接近的板级候选，包含电源域、U-Boot、Linux 4.9 配置、分区和启动参数。

## 2. 仓库定位

本仓库不是完整 Tina SDK，也不是当前可直接独立编译的完整 BSP。完整 SDK、厂商预编译组件和工具链通过百度网盘或供应商渠道获取。

计划拆分：

- `k1-v851s-bsp`：可公开的板级 DTS、非显示驱动、构建脚本
- `k1-v851s-private`：显示驱动、显示时序、校准、预编译组件和生产配置

## 3. 公开边界

计划开放：

- K1 板级 DTS 和 U-Boot 配置
- Linux 内核配置、分区和启动参数
- 音频、传感器、触摸、电源和输入驱动
- 构建和烧录说明

不开放：

- 显示驱动、面板初始化和寄存器时序
- Gamma、亮度、颜色和均匀性校准
- 厂商受限二进制库
- 量产固件、生产测试和签名私钥
- PCB、Gerber、完整 BOM、贴片和装配资料

## 4. 当前发布阻断项

- 非显示驱动源码尚未导入
- K1 专属引脚和器件配置尚未从候选板级配置中完全拆分
- 显示相关节点仍需复核并排除
- Allwinner 文档和工具再分发权尚未确认
- 干净环境全量构建和刷机验证尚未完成

本仓库当前以 Public Developer Preview 提供。上述问题仍是已知限制，不应据此认定该仓库已经完成量产级 BSP，也不代表已取得厂商文档或工具的再分发授权。

## 5. 许可证

K1 原创 BSP 代码采用 GPL-2.0-only。厂商文档、工具、预编译组件和第三方代码继续遵循其原始许可证，详见 [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md) 和 [LICENSE-NOTICE.md](LICENSE-NOTICE.md)。

## 6. 完整资料下载

- [百度网盘下载](https://pan.baidu.com/s/1eL-c3V66wPL7c91cLX-_5A?pwd=33pb)
- 提取码：`33pb`
- 分享目录：`k1`

详细下载和安全边界见 [K1 下载与使用说明](https://github.com/k1-open/k1-docs/blob/main/docs/download.md)。

## 7. 支持

- 邮箱：liuzemin@intel-platform.com
- 固定电话：26405693