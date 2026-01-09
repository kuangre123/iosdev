# App Store 上架流程（中国区）

## 1. App Store Connect 创建应用
- 选择正确的 Bundle ID 与 Team
- 填写 SKU（内部标识）
- 主要语言建议包含“简体中文”

## 2. 必填元数据
- 应用名称、副标题、类别、年龄分级
- 版权信息与联系信息
- 应用描述、关键词、技术支持网址

## 3. 资源准备
- 1024x1024 应用图标（PNG，无透明）
- 截图至少一套（建议 iPhone 6.7" 分辨率）
- 可选：预览视频（不必做也可审核）

## 4. 隐私与合规
- 隐私政策网址（必须是可公开访问网页）
- App Privacy 中如实填写数据收集与用途
- 若使用追踪/广告，需评估 ATT 与弹窗

## 5. 审核信息
- 提供审核备注（如测试账号、登录方式）
- 若功能需要账号，必须提供可用测试账号

## 6. 提交审核与发布
- Xcode Archive → Validate → Upload
- App Store Connect 选择构建版本并提交审核
- 通过后可手动发布或定时发布

## 7. 中国区注意事项（可能适用）
- 若涉及内容分发、UGC、地图/定位、医疗、教育、金融、游戏等，可能需要额外资质或合规说明
- 建议提供中文隐私政策与用户协议
- 以上要求以最新 Apple 审核政策与监管要求为准

## 官方参考链接
- App Store Connect: https://appstoreconnect.apple.com
- 审核指南: https://developer.apple.com/app-store/review/guidelines/
