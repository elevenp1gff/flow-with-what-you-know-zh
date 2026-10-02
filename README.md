# 顺着你已知的东西而“流” · Flow With What You Know（中文翻译版）

ICLR Blogposts 2025 文章 **Flow With What You Know**（作者：Scott H. Hawley，Belmont University / Hyperstate Music, Inc.）
的**全中文翻译**，含原文全部插图与三段动画。

## 怎么打开

- **`index.html`** —— 单文件网页，**图片与 3 段动画（MP4）已全部内嵌**，离线可看，动画自动循环播放。
  下载后用浏览器打开即可；也可以开启 GitHub Pages 直接在线访问。
- **`Flow_With_What_You_Know_zh-en.pdf`** —— 中英对照排版版（A4，39 页，带 PDF 书签目录），适合打印或通读原文。

## 内容简介

这篇文章用**基础物理**（而不是概率论）的视角讲清楚 flow matching（流匹配）与 rectified flow：

把速度场类比成风场图——空间中每一点都有速度矢量，空气沿流线运动，而**流线永不相交**；
训练时把源点与目标点随机配对、走直线，必然产生大量交叉轨迹，
但模型学到的是这些粒子运动的**聚合（“平均掉”）结果**，即分布层面的整体流动；
随后用 **Reflow** 把弯曲轨迹拉直（本质是教师—学生式的蒸馏），
再配合**时间扭曲**（弯曲处加密采样）与 **RK4** 积分（精度更高、总函数求值反而更少）加速采样。
最后把这一框架与扩散模型、最优传输、归一化流联系起来。

## 原文与出处

- 原文：ICLR Blogposts 2025 — *Flow With What You Know*，Scott H. Hawley
- 原文链接：<https://d2jud02ci9yv69.cloudfront.net/2025-04-28-flow-with-what-you-know-38/blog/flow-with-what-you-know/>
- 可执行 Colab：<https://colab.research.google.com/drive/1LfFgfvykgZOi9fcduE_Zkt1QYJxPKNtx>

## 说明

- 本仓库是**个人学习用途的非官方翻译**，未获原作者授权。
- 原文的**文字、图片、动画与代码版权均归原作者所有**；参考文献保留英文题录。
- 译文、排版与离线归档由本仓库维护者完成。若原作者或版权方有异议，将立即删除。

## 制作方式

离线抓取原文 → 提取结构化内容 → 逐段翻译 → 打包为自包含单文件网页
（图片与 MP4 以 base64 内嵌），并另出一版中英对照 PDF。
