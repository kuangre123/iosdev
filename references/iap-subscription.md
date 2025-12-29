# IAP 订阅配置与测试

## 1. 创建订阅组与产品
- App Store Connect → 功能 → App 内购买项目
- 创建订阅组（如 Premium）
- 新增自动续订订阅（Monthly/Yearly）
- 产品 ID 建议：`{BundleID}.premium_monthly`

## 2. 本地化与定价
- 填写显示名称与描述（简体中文必填）
- 选择价格档位
- 设置可用国家/地区（中国区为重点）

## 3. 订阅条款与展示
- 应用内展示：价格、周期、自动续订说明
- 提供“管理订阅”入口
- 若使用自定义条款，需提供 EULA/服务协议链接

## 4. 测试流程
- 创建沙盒测试账号（App Store Connect）
- 设备退出真实 Apple ID，使用沙盒账号购买
- 验证：购买成功、恢复购买、续订状态刷新

## 5. 常见问题
- 产品加载失败：检查产品 ID 与 Bundle ID 是否匹配
- 购买失败：检查是否登录沙盒账号、网络与设备购买限制
- 审核拒绝：提供清晰的订阅说明与恢复入口

## 官方参考链接
- In-App Purchase: https://developer.apple.com/in-app-purchase/
- 订阅最佳实践: https://developer.apple.com/app-store/subscriptions/
