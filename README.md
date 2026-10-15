# 越说 OfferFluent

用自己的简历和目标岗位练英文面试，再和 AI 教练重练表达。

产品网站：https://offerfluent.com

## 参赛作品

本次提供 V175 Web 源码、四页项目说明与实际网站操作视频。

- [完整可运行 Web 源码 ZIP](https://github.com/zengjingtao5775-droid/offerfluent/releases/download/shanghai-v175/OfferFluent-V175-Source.zip)
- [项目说明 PDF](https://github.com/zengjingtao5775-droid/offerfluent/releases/download/shanghai-v175/OfferFluent-Shanghai-Project-Introduction-V175.pdf)
- [约79秒操作演示 MP4](https://github.com/zengjingtao5775-droid/offerfluent/releases/download/shanghai-v175/OfferFluent-Shanghai-Demo-V175.mp4)
- [文件 SHA256](https://github.com/zengjingtao5775-droid/offerfluent/releases/download/shanghai-v175/SHA256SUMS.txt)

**完整应用代码在上面的专门源码附件中。** GitHub 自动生成的 “Source code (zip/tar.gz)” 只对应本仓库目录，请使用 `OfferFluent-V175-Source.zip` 查看和运行完整应用。

## 本机运行

下载并解压完整源码，在 `OfferFluent-V175/` 目录按 README 操作。需要 Node.js 24 和 pnpm 11.7.0。

```sh
pnpm install --frozen-lockfile
cp .env.example .env.local
node scripts/review-db.mjs
```

保留数据库终端，在第二个终端运行 `pnpm dev`，打开 http://localhost:3000 。数据库只监听本机；不要把评审辅助数据库部署到公网。

默认不附带任何正式服务凭据。无密钥模式可运行页面、明确的 demo 面试准备与确定性测试；实时 AI 对话需要你自己的百炼工作空间和模型凭据，完整语音面试还需对应语音服务配置。模型和云账号不包含在源码中。

## 验证范围

独立目录生产构建通过，八个入选测试文件53项通过，新建本机SQLite的9项接口检查通过。具体范围见源码包 CHECKS.md。演示为实际网站页面帧的剪辑，虚构履历、键盘作答，包含真实AI追问、翻译、可编辑助答、原句纠错和收藏。

## 许可

自有应用代码采用 [MIT](LICENSE)。品牌名称、角色及商业美术不纳入代码许可；第三方组件、字体及emoji保留原许可，详见 [RIGHTS.md](RIGHTS.md) 和源码包内的 licenses/。
