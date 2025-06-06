
# 🧠 Llama-3B-Jailbreak

本仓库包含一个基于 **unsloth/Llama-3.2-3B-Instruct** 的微调版本，使用 **LoRA（低秩适配）** 技术，在自定义的越狱数据集上进行训练。目标是用于实验性研究，特别是理解大语言模型的安全性和对齐行为。

## 模型已上传至 Hugging Face
本仓库基于`unsloth/Llama-3.2-3B-Instruct` 进行微调，[Hugging Face上的越狱模型](https://huggingface.co/zemelee/qwen2.5-jailbreak)的基座为`Qwen/Qwen2.5-3B-Instruct`，并不完全一致。

## 🔍 模型概览

| 属性 | 说明 |
|------|------|
| 基座模型 | `unsloth/Llama-3.2-3B-Instruct` |
| 微调方法 | Unsloth（LoRA）微调 |
| 数据集 | 自建越狱数据集 |
| 目的 | AI 安全与越狱行为研究 |
| 量化支持 | 可选（如 4-bit / 8-bit） |
| 使用许可 | 仅限教育和科研用途 |

## 📚 数据集说明

本模型使用开发者自行构建的“越狱”对话数据集进行训练。所有数据均为人工构造并经过清洗过滤，用于研究模型在非受限状态下的响应机制。
本仓库仅提供数据集中的一条示例，为防止数据集被滥用，请将数据集使用需求发送邮箱到`zemel@stu.sicnu.edu.cn`，我会尽快回复到您。
> ⚠️ 注意：此数据集仅供学术研究使用，请确保合理合规地使用该数据！

> ⚠️ 注意：此模型不建议部署于面向公众的商业服务中!



## 📌 注意事项与伦理声明

- 本模型可能生成有害、违法或不道德的内容，因其训练目标是为了探索边界行为。
- 请**仅用于学术研究**，不要用于生产系统。
- 在任何公开场景中使用前，请务必添加伦理防护措施。
- 未经授权不得随意发布或部署。



## 📬 链接
视频教程：[BILIBILI](https://www.bilibili.com/video/BV1zSJgztEKG)
📧 E-mail: `zemel@stu.sicnu.edu.cn`  
🐱 GitHub: [https://github.com/zemelee](https://github.com/zemelee)

---

## ⚖️ 免责声明

本模型仅供研究用途。作者不鼓励也不支持任何技术滥用行为。

---

> ✅ 本仓库由 [Zemelee](https://github.com/zemelee) 创建并维护。感谢您的关注与支持！



