
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
| 目的 | ~~好好玩呀~~ AI安全与越狱行为研究|


## 📚 数据集说明

本模型使用开发者自行构建的“越狱”对话数据集进行训练。数据集构造流程：



1. **初始种子数据筛选**  
   从已有的[开源越狱实验](https://github.com/JailbreakBench/artifacts/blob/main/attack-artifacts/JBC/manual/vicuna-13b-v1.5.json)中收集并筛选出危险问答对，作为初始的“越狱成功”样本集合。这些样本构成微调的第一阶段种子数据。

2. **初步微调**  
   利用上述种子数据对LLaMA进行微调，使其具备一定的绕过安全机制的能力。此阶段的目标是获得一个具备初步越狱响应能力的“攻击模型”。

3. **主动采样与扩展**  
   使用当前版本的攻击模型对[大规模潜在危险prompt数据集](https://github.com/STAIR-BUPT/JailBench/blob/main/JailBench_seed.csv)进行推理，从中筛选出模型成功输出违规内容的响应结果，形成新的越狱问答对。

4. **迭代增强训练**  
   将新生成的越狱样本加入训练数据集，进一步微调模型。随着每一轮迭代，模型的越狱能力不断增强，同时能够生成更多新颖、复杂、具有挑战性的越狱响应。

5. **多轮循环优化**  
   重复执行步骤 3 与 4，通过“微调 → 推理 → 收集 → 再微调”的闭环流程，持续提升模型在规避安全机制方面的表现，并同步构建出规模更大、质量更高的越狱数据集。

6. **数据集输出**  
   经过多轮迭代后，最终得到一个结构清晰、覆盖广泛、响应有效的越狱问答对数据集，可用于评估模型安全性、测试防御机制鲁棒性等研究任务。

> ⚠️ 注意：此数据集仅供学术研究使用，请确保合理合规地使用该数据！
> ⚠️ 危险答案数据集，本仓库也许是全网首发。危险问题很好找，危险答案很罕见，且用且珍惜。



## 📌 注意事项与伦理声明

- 本模型可能生成有害、违法或不道德的内容，因其训练目标是为了探索边界行为。
- 请**仅用于学术研究**，不要用于生产系统。
- 在任何公开场景中使用前，请务必添加伦理防护措施。
- 未经授权不得随意发布或部署。



## 📬 链接

📺 视频教程：[BV1zSJgztEKG](https://www.bilibili.com/video/BV1zSJgztEKG)

🤗 Hugging Face：[qwen2.5-jailbreak](https://huggingface.co/zemelee/qwen2.5-jailbreak)

📧 E-mail: `zemel@stu.sicnu.edu.cn`  

🐱 GitHub: [https://github.com/zemelee](https://github.com/zemelee)

🤖 线上体验：[sugarblack](http://test.sugarblack.top)

😚 微信公众号： 做实验的研究牲

---

## ⚖️ 免责声明

本模型仅供研究用途。作者不鼓励也不支持任何技术滥用行为。

---

> ✅ 本仓库由 [Zemelee](https://github.com/zemelee) 创建并维护。感谢您的关注与支持！



