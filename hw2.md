# Hw2 Classification 思路
- 多加幾層 Linear
- concat_nframes 設 21，爆 RAM 的話可調小 preprocess_data 中的 max_len（2200000 不會有 truncation 的問題）
- 若覺得自己模型太強，可使用 dropout 防止 overfitting
- AdamW betas 用 (0.9, 0.98)
- lr 1e-3，train 約 10 ~ 20 epochs, batch size 512 上下，可自行調整（很閒的話也可以用 batch size 4）
## Boss Hints
- 如跑完一 epoch 突然出現維度錯誤，注意 drop_last（test 不能用）
- 注意維度，善用 view 跟 transpose
- 修改 truncation 跟 padding 以用更高的 concat_nframes
- 不要用 RNN，用 GRU 或 Transformer Block
- 可以參考 transformers 的 Hubert 的 Feature Encoder，用 Conv1d、GELU、LayerNorm，但要改一下酷酷的 LibriDataset 避免爆 RAM（可能要想一下怎麼重複利用 memory）。
## 心得
- 我本人的專題是做 Spoken Language Understanding, 常常拜讀（跪著）宏毅老師的論文（SUPERB 真的很厲害），覺得老師這次作業出得相當好，雖然知識量有點多，希望大家能努力搞懂 > <。另外推個陳縕儂老師的 miuLab，老師人真的很好，歡迎各位來當我的學弟妹呦～～
