# quar
quar(夸娥)，a little large LM
**其他语言版本: [English](README_en.md), [中文](README.md).**
quar(k),夸娥氏是中国古代神话中的大力神，其二子助愚公移山。九层之台起于垒土，九天巨人起于夸克，希望这个小模型，能成为我求学过程中的quark。

## 计划
- [x] 初步分析
- [ ] 技术选择
- [ ] 预训练
- [ ] 对齐

## 初步分析
### 硬件
8卡4090（FP16算力 330 Tflops，FP32算力 83 Tflops；24 GB内存）。

### 预训练所需算力
如果以[CLUECorpusSmall](https://paddlenlp.readthedocs.io/zh/latest/llm/pretraining/data/CLUECorpusSmall.html)为预训练数据集，14GB中文预料，每2汉字1token估算，共需喂给模型$$ \frac{14GB}{2byte*2}\approx 3e9 tokens $$
