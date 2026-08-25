# 工作整合管理系统

面向酒店用品销售公司的 Android 库存与客户关系管理应用。销售人员可以在手机上维护库存、登记入库和销售出库、管理客户与销售过程，并查看商品需求趋势。

## 主要功能

- 库存商品管理：商品类型、商品名称、库存数量、库存搜索和低库存提醒
- 快速业务操作：入库、销售出库、数量校验和操作记录
- 客户管理：客户档案、联系人、电话、城市、级别、备注和客户详情
- CRM 工作台：线索、商机、报价、合同、营销活动和服务工单
- 代办计划：拜访计划和待办事项，支持按提前天数提醒
- 数据分析：按客户和商品类型查看去年各月份需求量，支持多商品曲线、月份间距和端点数值显示
- 设置：低库存提醒开关、商品类型维护和业务数据清除

## 技术说明

- Android 原生容器 + WebView 本地页面
- 业务数据保存在手机本地，不依赖网络、Google Play Services 或 HMS
- 包名：`com.codex.inventorysales.v01`
- 版本：`0.1`（versionCode `10`）
- 最低 Android 版本：Android 6.0（API 23）
- 目标编译版本：Android 14（API 34）

应用可在 Android 和多数支持 Android APK 的华为手机上运行。HarmonyOS NEXT 是否兼容 Android APK 取决于具体设备版本和系统策略，本项目不对此作保证。

## 使用 Android Studio 构建

1. 使用 Android Studio 打开本目录。
2. 等待 Gradle 同步完成。
3. 选择 `Build > Build APK(s)`。
4. APK 输出在 `app/build/outputs/apk/debug/`。

项目中的 `local.properties` 仅用于本机 SDK 配置，不应提交到 Git。首次构建时请让 Android Studio 自动生成本机配置。

## 测试 APK

当前测试包位于 [`releases/debug-1-v01.apk`](releases/debug-1-v01.apk)。该 APK 使用 debug 签名，仅用于开发测试，不适合直接发布到应用市场。安装前请确认手机允许安装对应来源的应用。

## 数据说明

应用使用本地存储，卸载应用或使用设置中的“清除数据”会使当前设备上的业务数据丢失。正式部署到多设备协作环境前，需要接入服务端账号、权限和数据同步能力。
