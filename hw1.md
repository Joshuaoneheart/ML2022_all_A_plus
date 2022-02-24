# HW1 Regression 思路
- Model 留 input layer 跟 output layer, hidden dim 隨便設
- Feature selection: \[53, 67, 69, 85, 101, 102, 103, 115\] (此feature 由 LightGBM 依重要性篩出), select_all 改 false
- Batch size 越小越好，不知道為什麼代表你沒有好好看上課影片
- optimizer: AdamW(from Transformers), lr 5e-4 ~ 1e-5 皆可，可自行調整，betas=(0.9, 0.98)(根據 Attention is All you Need, https://proceedings.neurips.cc/paper/2017/file/3f5ee243547dee91fbd053c1c4a845aa-Paper.pdf)
- 跑 500 epochs, early stop 50, 視個人需求自行調整
