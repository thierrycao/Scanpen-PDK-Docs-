# Scanpen PDK 开发说明

本目录托管 Scanpen PDK 接口开发说明页面，当前内容基于 `v0.0.3-pdk-b9702d79` / `exp-v0.0.3-pdk-b9702d79-1-g4e26b81a` / commit `4e26b81a` 整理。

## 在线入口

- 文档页面：`index.html`
- 推荐本地预览：直接用浏览器打开 `index.html`，或在本目录启动静态服务。

```bash
python3 -m http.server 8080
# 浏览器访问 http://127.0.0.1:8080/
```

## 仓库信息

- Scanpen PDK 仓库：`https://cloud.listenai.com/CSKG836746/arcs-sdk/public/scanpen.git`
- 文档目录：`docs/scanpen/docs/scanpen-pdk-api/`

## 文档覆盖范围

- 快速上手：环境搭建、Git LFS、编译、烧录、分区和 OTA。
- 架构说明：PDK 目录结构、运行时分层、启动链路。
- 接口开发：PDK 消息总线、Scan 消息域、`scan_server` API、`pdk_invoke`。
- 产品能力：LVGL/AuraUI UI 接入、RTC 定时闹钟、经典蓝牙耳机、USB CDC 校准、摄像头帧接口。
- 调试排障：构建烧录命令、Shell 调试、源码索引。

## 版本更新摘要

扫描笔 PDK V0.0.3-alpha.0：

- 修改系统分区，扩展 CP 应用固件分区大小以支持业务开发。
- 更新 boot 程序，优化系统兼容性。
- 新增 Flash2 区域链接数据段，编译输出独立的 Flash2 镜像文件。
- 优化系统流程，支持快速扫描。
- 新增 MSC 模式支持，使用 shell 命令进行模式切换。

## 维护说明

- 如果 `apps/scanpen/res/partitions.yaml` 调整，需同步更新文档中的分区表、烧录地址和 OTA 说明。
- 如果 `apps/scanpen/prj.conf` 或蓝牙、RTC、UI 启动链路变更，需同步更新对应章节。
- 修改 `index.html` 后建议检查左侧目录锚点和页面渲染。
