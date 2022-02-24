# Hw7 BERT 思路
- 中文可以用 hfl/chinese-macbert-large 或 hfl/chinese-roberta-wwm-ext-large（印象中 macbert 比較好）
- huggingface transformers 的文件寫的蠻清楚的，還有 source code 可以看：https://huggingface.co/docs/transformers/index
- max_paragraph_len 跟 doc_stride 應該要不一樣
- max_paragraph_len 跟 max_question_len 應該要盡量長（注意 Bert 的最大輸入長度 512，還須考量 [CLS] 跟 [SEP]），具體多長可以統計一下資料集中最長的問題跟文章長度
- 可以不要在 train 時固定取 answer 在中間的 window，會讓 model 覺得答案一定在中間附近，也許可以增加一點隨機性？
- 這裡有一篇比較 roberta-wwm-ext 跟 macbert 的論文：https://arxiv.org/abs/2004.13922 
## Boss hint
- start_index 有可能比 end_index 大，導致輸出答案為空，可能要想辦法解決這個情形？
