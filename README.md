# 光学宝典 · Optics Bible

移动端光学设计与仿真工作台。手机负责界面、即时预览与轻量交互，重计算与模型调度由「光屿服务端」承担，两端通过统一的 `/api/v1` 接口通信。

本仓库只承载发布产物与文档，不存放源码与运行产物。

## 下载

最新版本在 Releases 页面发布，包含两个文件：

| 文件 | 说明 | 版本 |
| --- | --- | --- |
| `MeowOptics-v151-test64.apk` | Android 客户端，Android 8.0 及以上 | versionCode 152 / 2.0.0-test.64 |
| `Guangyu-Server.exe` | 光屿服务端，Windows 免安装便携版 | 随包发布 |

下载地址：https://github.com/Alice-P197/optics-bible/releases/latest

直链：

- 客户端：https://github.com/Alice-P197/optics-bible/releases/download/v151-test64/MeowOptics-v151-test64.apk
- 服务端：https://github.com/Alice-P197/optics-bible/releases/download/v151-test64/Guangyu-Server.exe

## 安装

### Android 客户端

1. 下载 APK 后直接安装。若已安装旧版本，签名一致可直接覆盖，无需卸载。
2. 首次启动允许通知与文件访问权限。
3. 连接服务端两种方式：同一局域网自动发现，或在设置中手动填服务端地址。

签名指纹（SHA-256）：`56222efc627b6e9f475bd4bd3940d168b202e9ae4123676e042e9736d149f151`

### 光屿服务端

1. 解压后双击 `Guangyu-Server.exe`（光屿服务端）。
2. 启动后监听三个端口：`8790` HTTP 网关、`8793` Python 后端、`8791` UDP 局域网发现。
3. 手机与服务端在同一网络时自动发现；跨网络需在客户端手动填写服务端地址，并在防火墙放行上述端口。

## 能力

客户端

- 光学手册库：分类检索、分页浏览
- 镜头设计：预设选型、面型编辑、指标分析、2D 布局与 3D 视图
- 计算器：常用光学公式与参数换算
- 技能库：镜头设计、膜系、衍射、照明等专项流程
- 模板库：常用结构一键套用
- 对话式设计：模型选择、深度思考、联网检索、技能调用、产物管理

服务端

- `/api/v1/health`、`/models`：健康检查与可用模型
- `/api/v1/lens`：镜头设计、优化、指标与出图
- `/api/v1/py/exec`、`/pip/*`：Python 计算与依赖
- `/api/v1/files`、`/artifacts`：文件与产物
- `/api/v1/plot`：通用曲线交互页
- `/api/v1/jobs/{id}`：异步任务查询

## 版本

当前发布 `2.0.0-test.64`（versionCode 152）。测试版，用于真机验收；正式版将升级为云端架构（账号体系、服务端模型调度、产物云存储）。

## 说明

- 本仓库不含生成产物、运行日志与本地配置。
- 服务端源码与客户端源码在私有仓库维护。
</content>
