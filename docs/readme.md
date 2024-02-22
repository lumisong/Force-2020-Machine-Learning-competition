# FORCE 2020 Machine Learning Competition 竞赛

## Lithology prediction 地层预测

岩性预测竞赛的目标是为提供的井记录、挪威石油局岩性地层学和井X、Y位置正确预测岩性标签。

TODO:分析数据处理，关于输入特征：Well logs，地层学，位置（X，Y），输出特征：岩性标签

比赛采用罚分矩阵进行评分。有些标签错误会比其他错误受到更多惩罚,请参阅入门笔记本和惩罚矩阵了解详细信息。

TODO:入门笔记本和惩罚矩阵；模型评估，指标部分，融合了惩罚系数。位置：lithology_competition/data文件夹

所有数据集和入门笔记本都可以在lithology_competition/data下找到。

原始文件：**文件和标准的测井las文件，所有的csv文件数据，预测和提交的模型和权重**也可以在这里找到，还有许多其他免费的地质地下数据。该文件夹名为FORCE 2020岩相预测来自测井竞赛（[https://drive.google.com/drive/folders/0B7brcf-eGK8CRUhfRW9rSG91bW8）](https://drive.google.com/drive/folders/0B7brcf-eGK8CRUhfRW9rSG91bW8%EF%BC%89)

### Results of final scoring 最终结果得分，分析

TODO：结果总结内容 [bolg - 岩相竞赛地质总结.pdf]

| 队伍 | 排行榜 score | Leaderboard rank 排名 | Final test score 测试 | Final rank 总结得分|
|---|---|---|---|---|
| Olawale Ibrahim | -0.5118 | 24 | -0.4690 | 1 |
| GIR Team | -0.5037 | 11 | -0.4792 | 2 |
| Lab.ICA-Team / Smith A. | -0.4943 | 6 | -0.4954 | 3 |
| H3G (Haoyuan Zhang, Harry Brandsen, Gregory Barrere, Helena Nandi Formentin) | -0.509 | 17 | -0.5045 | 4 |
| ISPL Team | -0.4885 | 2 | -0.5084 | 5 |
| Jiampiers C. | -0.5014 | 9 | -0.5087 | 6 |
| José Bermúdez | -0.5052 | 14 | -0.5091 | 7 |
| Bohdan Pavlyshenko | -0.5112 | 22 | -0.5171 | 8 |
| Jeremy Zhao | -0.5264 | 31 | -0.5173 | 9 |
| Campbell Hutcheson | -0.505 | 13 | -0.5221 | 10 |
| David P. | -0.4775 | 1 | -0.5256 | 11 |
| SoftServe Team | -0.4936 | 3 | -0.5263 | 12 |
| Dapo Awolayo | -0.5121 | 25 | -0.9441 | 13 |
