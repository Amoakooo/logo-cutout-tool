# LOGO抠图工具

这是一个无需安装的软件版本，直接用浏览器打开即可使用。

## 使用方法

1. 打开 `index.html`
2. 把图片拖进页面，或点击选择图片
3. 调整“去除范围”和“边缘柔化”
4. 如有封闭背景残留，点击“点选封闭背景”，再点一下要清除的位置
5. 在“下载画质”中选择原始画质、AI 增强 2 倍或 AI 增强 3 倍
6. 选择 AI 画质时，点击“开始 AI 增强”，通过进度条查看处理进度
7. 进度达到 100% 后，点击“下载增强 PNG”
8. 原始画质无需增强，可以直接下载
9. 如果手机没有自动下载，点击绿色的“打开/长按保存 PNG”，再长按图片保存

AI 画质增强使用开源 UpscalerJS 与 ESRGAN Slim 超分辨率模型，默认保持原始画质。首次使用 AI 增强需要联网加载模型。为避免手机内存不足，超大图片会自动限制处理尺寸。

绿色的“打开/长按保存 PNG”仅在手机或触屏设备显示，电脑端会直接下载。

## 开源画质增强

- [UpscalerJS](https://github.com/thekevinscott/UpscalerJS)（MIT License）
- [ESRGAN Slim 模型](https://upscalerjs.com/models/available/upscaling/esrgan-slim/)
- [TensorFlow.js](https://github.com/tensorflow/tfjs)（Apache-2.0 License）

## 部署到 GitHub Pages

1. 在 GitHub 新建一个仓库
2. 上传本文件夹里的 `index.html` 和 `README.md`
3. 打开仓库的 `Settings`
4. 进入 `Pages`
5. 在 `Build and deployment` 里选择 `Deploy from a branch`
6. Branch 选择 `main`，文件夹选择 `/root`
7. 保存后等待 GitHub 生成访问链接

## 适合处理

- 白底产品图
- 纯色背景图片
- 浅色背景电商图
- 背景从图片边缘连通的图片

## 说明

这个版本会优先删除从图片边缘连通进来的背景，可以减少白衬衫、浅肤色等主体区域被误删的情况。

遇到字母、标志、图形内部的封闭背景时，可以使用“点选封闭背景”手动清除。可以连续点选多处，也可以点击“清空点选”重新来。

如果背景很复杂，或者主体和背景颜色非常接近，纯浏览器版可能无法做到专业 AI 抠图的效果。
