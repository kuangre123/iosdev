# iOS 开发与构建要点

## 1. 基础信息确认
- App 名称、Bundle ID、Team
- 最低 iOS 版本
- 是否包含推送/后台/定位/相机/麦克风/订阅等能力

## 2. 依赖管理
- **Swift Package Manager**: 推荐优先使用，便于审计
- **CocoaPods**: 需要 Podfile 与 workspace 管理
- **注意**: 依赖升级需评估 API 变更与许可风险

## 3. 版本号与构建号
- **Version**: `CFBundleShortVersionString`（用户可见）
- **Build**: `CFBundleVersion`（每次上传必须递增）
- 建议规则：`1.2.3` + `YYYYMMDDHHMM` 或 `自增整数`

## 4. 签名与证书（简化原则）
- 开发阶段：Development 证书 + Development Profile
- 发布阶段：Distribution 证书 + App Store Profile
- Xcode 推荐开启 **Automatically manage signing**
- 多目标/多环境需确认签名一致性

## 5. 构建与归档
- Xcode: **Product → Archive**
- CI/命令行：
  - `xcodebuild archive` 生成 `.xcarchive`
  - `xcodebuild -exportArchive` 导出 `ipa`
- 上传前建议 **Validate** 归档

## 6. 常见问题排查
- **签名错误**: 检查 Team/Bundle ID/Provisioning 是否匹配
- **依赖冲突**: 清理 DerivedData，核对锁定版本
- **构建失败**: 检查最低 iOS 版本与依赖兼容性
