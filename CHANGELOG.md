## 1.0.1（2026-11-08）

- 补齐 Android 导航布局的 RecyclerView 1.3.2 依赖，修复缺类导致的导航视图创建失败；更新后须重新制作自定义基座或原生安装包。
- 补充宿主根 AndroidManifest.xml 的 TencentMapSDK 元数据及本地 manifestPlaceholders.json 配置，明确动态初始化 Key 不能代替导航底图的原生配置。
- 修正 Android 驾车数据就绪事件的会话 ID 语义：新增 navSessionId 及算路回包会话标识，旧 routeId 仅为明确弃用的会话别名；真实路线选择仍使用 routes[n].routeId。
- 补充 Android Native 真机地图与模拟导航截图，已观察真实路线、开始/停止和 TTS 回调；本轮按真实导航会话匹配的原生协议通过，8 次 Native 回调均一次/主线程/code=0。保留 UTS/uvue、iOS、GPS 与实际可听语音的验证边界。

## 1.0.0（2026-11-07）

新增腾讯原生地图与导航封装；新增本地离线轨迹记录、分段回放、导出和删除。具体编译与尚未完成的在线服务验证见README与验收记录。
