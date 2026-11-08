# Android 宿主配置模板

这些文件仅为公开配置模板，不包含可用 Key，也不是可单独运行的插件或应用。

1. 将 `AndroidManifest.xml.example` 的 `<meta-data>` 合并到你自己的宿主根 `AndroidManifest.xml`，包名替换为实际包名。已有文件保留其他节点，避免重复 `application` 或元数据。
2. 将 `manifestPlaceholders.example.json` 复制到宿主 `nativeResources/android/manifestPlaceholders.json`，在本机填入自己的 Android Client Key。
3. 初始化 API 的 `key` 使用同一个 Client Key，并在取得用户隐私同意后调用。仅动态初始化不能替代导航底图的 Manifest 配置。
4. 重新打包自定义基座 / 原生安装包，确认腾讯控制台的授权应用与实际包名一致。

真实占位符配置必须排除在 Git 提交之外。Client Key 会进入客户端安装包，需配置平台限制；服务端 SecretKey 不可进入客户端。

完整接入示例见[插件文档](../../docs/api-and-setup.md)。配置机制参考[DCloud 官方 Android 原生清单与资源文档](https://doc.dcloud.net.cn/uni-app-x/collocation/app-nativeresource-android.html)。
