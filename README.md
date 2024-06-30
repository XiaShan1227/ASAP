【AAAI-2020 ASAPooling】[ASAP: Adaptive Structure Aware Pooling for Learning Hierarchical Graph Representations](https://arxiv.org/abs/1911.07979)
![image](https://github.com/XiaShan1227/ASAP/assets/67092235/9df3314c-1413-4f39-ab9d-5f4c5aa1059b)


1.实验参数
| **Parameter** | **Value** |
|:-------------| :------------:|
| Batch size | 128 |
| Dataset | 可选: DD、MUTAG、NCI1、NCI109、PROTEINS, etc |
| Dropout ratio | 0.5 |
| Epochs | 10000 |
| Exp name | 自命名: DD_Glo、MUTAG_Hie, etc |
| Gpu index | 0 |
| Hid | 128 |
| Lr | 0.0005 |
| Model | 可选: ASAPooling_Global、ASAPooling_Hierarchical |
| Patience | 40 |
| Pooling ratio | 0.5 |
| Seed | 16 |
| Test batch size | 1 |
| Weight decay | 0.0001 |

2.运行程序 </br>
模型：ASAPooling_Global </br>
数据集：DD
```python
python main.py --exp_name=DD_Glo --dataset=DD --model=ASAPooling_Global
```

模型：ASAPooling_Hierarchical </br>
数据集：PROTEINS
```python
python main.py --exp_name=PROTEINS_Hie --dataset=PROTEINS --model=ASAPooling_Hierarchical
```

3.实验结果（8:1:1划分数据集，只做了一次实验的准确率，保留两位小数）
| | **DD** | **MUTAG** | **NCI1** | **NCI109** | **PROTEINS** |
|:-------------:|:-------------:|:------------:|:------------:|:------------:|:------------:|
| **ASAPooling_Global**       |  61.34  |  80.00  |  64.48  |  73.91  |  73.21  |
| **ASAPooling_Hierarchical** |  65.55  |  70.00  |  76.89  |  73.19  |  77.68  |
