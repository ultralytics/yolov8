<div align="center">
  <p>
    <a href="https://platform.ultralytics.com/?utm_source=github&utm_medium=referral&utm_campaign=platform_launch&utm_content=banner&utm_term=yolov8_github" target="_blank">
      <img width="100%" src="https://raw.githubusercontent.com/ultralytics/assets/main/yolov8/banner-yolov8.png" alt="Ultralytics YOLO banner"></a>
  </p>

[中文](https://docs.ultralytics.com/zh) | [한국어](https://docs.ultralytics.com/ko) | [日本語](https://docs.ultralytics.com/ja) | [Русский](https://docs.ultralytics.com/ru) | [Deutsch](https://docs.ultralytics.com/de) | [Français](https://docs.ultralytics.com/fr) | [Español](https://docs.ultralytics.com/es) | [Português](https://docs.ultralytics.com/pt) | [Türkçe](https://docs.ultralytics.com/tr) | [Tiếng Việt](https://docs.ultralytics.com/vi) | [العربية](https://docs.ultralytics.com/ar) <br>

<div>
    <a href="https://github.com/ultralytics/ultralytics/actions/workflows/ci.yml"><img src="https://github.com/ultralytics/ultralytics/actions/workflows/ci.yml/badge.svg" alt="Ultralytics CI"></a>
    <a href="https://clickpy.clickhouse.com/dashboard/ultralytics"><img src="https://static.pepy.tech/badge/ultralytics" alt="Ultralytics Downloads"></a>
    <a href="https://discord.com/invite/ultralytics"><img alt="Ultralytics Discord" src="https://img.shields.io/discord/1089800235347353640?logo=discord&logoColor=white&label=Discord&color=blue"></a>
    <a href="https://community.ultralytics.com/"><img alt="Ultralytics Forums" src="https://img.shields.io/discourse/users?server=https%3A%2F%2Fcommunity.ultralytics.com&logo=discourse&label=Forums&color=blue"></a>
    <a href="https://www.reddit.com/r/ultralytics/"><img alt="Ultralytics Reddit" src="https://img.shields.io/reddit/subreddit-subscribers/ultralytics?style=flat&logo=reddit&logoColor=white&label=Reddit&color=blue"></a>
    <br>
    <a href="https://console.paperspace.com/github/ultralytics/ultralytics"><img src="https://assets.paperspace.io/img/gradient-badge.svg" alt="Run Ultralytics on Gradient"></a>
    <a href="https://colab.research.google.com/github/ultralytics/ultralytics/blob/main/examples/tutorial.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open Ultralytics In Colab"></a>
    <a href="https://mybinder.org/v2/gh/ultralytics/ultralytics/HEAD?labpath=examples%2Ftutorial.ipynb"><img src="https://mybinder.org/badge_logo.svg" alt="Open Ultralytics In Binder"></a>
</div>
</div>
<br>

[Ultralytics](https://www.ultralytics.com/) [YOLOv8](https://docs.ultralytics.com/zh/models/yolov8) 可通过官方
[Ultralytics YOLO](https://github.com/ultralytics/ultralytics) 包使用，支持目标检测、实例分割、图像分类、姿态估计和跟踪，并提供快速、准确、易用的 Python 与 CLI 工作流。

本仓库是 YOLOv8 的轻量级发现入口。官方实现、软件包发布、模型下载、Issues 和 Pull Requests 均在
[ultralytics/ultralytics](https://github.com/ultralytics/ultralytics) 仓库维护。

## 📄 文档

请参阅下文了解快速安装和 YOLOv8 使用示例。有关训练、验证、预测和部署的完整指南，请参阅
[Ultralytics 文档](https://docs.ultralytics.com/zh)。

<details open>
<summary>安装</summary>

在 [Python>=3.8](https://www.python.org/) 环境中安装 `ultralytics` 包，并使用
[PyTorch](https://pytorch.org/get-started/locally/)。

[![PyPI - Version](https://img.shields.io/pypi/v/ultralytics?logo=pypi&logoColor=white)](https://pypi.org/project/ultralytics/)
[![Ultralytics Downloads](https://static.pepy.tech/badge/ultralytics)](https://clickpy.clickhouse.com/dashboard/ultralytics)
[![PyPI - Python Version](https://img.shields.io/pypi/pyversions/ultralytics?logo=python&logoColor=gold)](https://pypi.org/project/ultralytics/)

```bash
pip install ultralytics
```

</details>

<details open>
<summary>使用方法</summary>

### CLI

```bash
yolo predict model=yolov8n.pt source="https://ultralytics.com/images/bus.jpg"
```

### Python

```python
from ultralytics import YOLO

# 加载预训练的 YOLOv8n 模型
model = YOLO("yolov8n.pt")

# 对示例图像运行推理
results = model("https://ultralytics.com/images/bus.jpg")

# 显示带标注的结果
results[0].show()
```

</details>

## ✨ 模型

YOLOv8 模型支持检测、分割、分类、姿态估计和旋转目标检测。所有模型权重都会在首次使用时从最新的 Ultralytics assets 发布版本自动下载。

<a href="https://docs.ultralytics.com/zh/tasks" target="_blank">
    <img width="100%" src="https://raw.githubusercontent.com/ultralytics/assets/main/docs/ultralytics-yolov8-tasks-banner.avif" alt="Ultralytics YOLO supported tasks">
</a>

| 模型系列                                                           | 示例权重                                                                                  | 任务                                                      | Train | Val | Predict | Export |
| ------------------------------------------------------------------ | ----------------------------------------------------------------------------------------- | --------------------------------------------------------- | ----- | --- | ------- | ------ |
| [YOLOv8](https://platform.ultralytics.com/ultralytics/yolov8)      | `yolov8n.pt` `yolov8s.pt` `yolov8m.pt` `yolov8l.pt` `yolov8x.pt`                          | [检测](https://docs.ultralytics.com/zh/tasks/detect)      | ✅    | ✅  | ✅      | ✅     |
| [YOLOv8-seg](https://platform.ultralytics.com/ultralytics/yolov8)  | `yolov8n-seg.pt` `yolov8s-seg.pt` `yolov8m-seg.pt` `yolov8l-seg.pt` `yolov8x-seg.pt`      | [实例分割](https://docs.ultralytics.com/zh/tasks/segment) | ✅    | ✅  | ✅      | ✅     |
| [YOLOv8-cls](https://platform.ultralytics.com/ultralytics/yolov8)  | `yolov8n-cls.pt` `yolov8s-cls.pt` `yolov8m-cls.pt` `yolov8l-cls.pt` `yolov8x-cls.pt`      | [分类](https://docs.ultralytics.com/zh/tasks/classify)    | ✅    | ✅  | ✅      | ✅     |
| [YOLOv8-pose](https://platform.ultralytics.com/ultralytics/yolov8) | `yolov8n-pose.pt` `yolov8s-pose.pt` `yolov8m-pose.pt` `yolov8l-pose.pt` `yolov8x-pose.pt` | [姿态估计](https://docs.ultralytics.com/zh/tasks/pose)    | ✅    | ✅  | ✅      | ✅     |
| [YOLOv8-obb](https://platform.ultralytics.com/ultralytics/yolov8)  | `yolov8n-obb.pt` `yolov8s-obb.pt` `yolov8m-obb.pt` `yolov8l-obb.pt` `yolov8x-obb.pt`      | [旋转目标检测](https://docs.ultralytics.com/zh/tasks/obb) | ✅    | ✅  | ✅      | ✅     |

## 🧩 集成

Ultralytics 集成扩展了数据集标注、训练、可视化、部署和模型管理工作流。了解
[Ultralytics Platform](https://platform.ultralytics.com) 和
[Ultralytics 集成文档](https://docs.ultralytics.com/integrations)，将 YOLOv8 连接到您的 AI 工作流，包括常用导出格式
[TensorRT](https://docs.ultralytics.com/integrations/tensorrt)、[ONNX](https://docs.ultralytics.com/integrations/onnx)、
[CoreML](https://docs.ultralytics.com/integrations/coreml) 和
[TFLite](https://docs.ultralytics.com/integrations/tflite)。

<a href="https://platform.ultralytics.com" target="_blank">
    <img width="100%" src="https://github.com/ultralytics/assets/raw/main/yolov8/banner-integrations.png" alt="Ultralytics active learning integrations">
</a>

## 🤝 贡献

我们依靠社区协作蓬勃发展！请参阅[贡献指南](https://docs.ultralytics.com/help/contributing)开始贡献。源码更改、文档改进、错误报告和功能请求请提交到官方
[ultralytics/ultralytics](https://github.com/ultralytics/ultralytics) 仓库。

[![Ultralytics open-source contributors](https://raw.githubusercontent.com/ultralytics/assets/main/im/image-contributors.png)](https://github.com/ultralytics/ultralytics/graphs/contributors)

## 📜 许可证

Ultralytics 提供两种许可选项以满足不同需求：

- **AGPL-3.0 许可证**：这种经 [OSI 批准](https://opensource.org/license/agpl-3.0)的开源许可证非常适合学生、研究人员和爱好者。有关完整详细信息，请参阅 [LICENSE](LICENSE) 文件。
- **Ultralytics 企业许可证**：适用于开发和生产用途，此许可证允许将 Ultralytics 软件和 AI 模型集成到业务产品和服务中，并绕过 AGPL-3.0 的开源要求。如需开始使用，请通过 [Ultralytics 授权许可](https://www.ultralytics.com/license)与我们联系。

## 📞 联系方式

- [YOLOv8 文档](https://docs.ultralytics.com/zh/models/yolov8)
- [Ultralytics Python 包](https://pypi.org/project/ultralytics/)
- [官方源代码](https://github.com/ultralytics/ultralytics)
- [支持与 Issues](https://github.com/ultralytics/ultralytics/issues/new/choose)

如有疑问、讨论和社区支持，请加入 [Discord](https://discord.com/invite/ultralytics)、[Reddit](https://www.reddit.com/r/ultralytics/)
和 [Ultralytics 社区论坛](https://community.ultralytics.com/)。
