# Hw8 Anomaly Detection
- 用 torchvision 上的模型（注意不能用 pretrained），拿幾個當 encoder（我用 resnet18 和 efficientnet_b3） 把 output 加起來再丟到 decoder（我用 fcn），用 fcn 需注意 flatten
- 這方法有點偷吃步，想認真做可以多研究 anomaly detection 相關的論文（如 PaDiM、STFPM）
## Boss hint
- anomalib 上統整了蠻多相關的論文，但是通常要轉成圖片才能用，或是不一定有 anomaly score，可以試著用用看？
