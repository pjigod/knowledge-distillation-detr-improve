# knowledge-distillation-detr-improve

本仓库用于 DETR 知识蒸馏实验，基于 [KD-DETR](https://github.com/wennyuhey/KD-DETR)。方法使用一致的蒸馏点，让学生模型学习教师模型的检测能力。

## 本仓库包含

- KD-DETR 模型与蒸馏训练代码。
- DAB-DETR-R50 教师模型、DAB-DETR-R18 学生模型的训练配置。
- 训练与测试脚本。

## 蒸馏训练

按原项目说明准备 COCO 数据集和教师模型权重，并检查脚本中的数据、权重路径。

```bash
cd KD-DETR
pip install -r requirements.txt
sh tools/train.sh exp1
```

`train.sh` 默认使用 Linux 环境和 8 张 GPU；使用其他环境时需要修改脚本配置。

## 相关仓库

- [RT-DETR 基线仓库](https://github.com/pjigod/knowledge-distillation-detr-baseline)

## 来源

- 上游代码：[wennyuhey/KD-DETR](https://github.com/wennyuhey/KD-DETR)
- 论文：[KD-DETR，CVPR 2024](https://openaccess.thecvf.com/content/CVPR2024/html/Wang_KD-DETR_Knowledge_Distillation_for_Detection_Transformer_with_Consistent_Distillation_Points_CVPR_2024_paper.html)
