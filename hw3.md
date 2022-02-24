# Hw3 Image Classification 思路
- VGG 11, 16, 19、ResNet、SimCLR（來鬧），各種架構都試試看，我是用 VGG11
- 因為有用 BatchNorm，Batch size 大比較好，128 不會爆 VRAM
- AutoAugment 是個好東西，其他能用的 augmentation 還有很多，比如 ColorJitter、RandomAffine、RandomHorizontalFlip 之類的
- 4 epochs 明顯太少，硬 train 20000000 個
- optimizer 同 hw2
- 自我工商一下可以去看我去年的 hw3 的扣（README 裡有 link），再次提醒，不行抄襲，被抓請自行負責
- torchvision 有酷酷的模型架構可以 import，只要不用 pretrained 就不算用 pretrained model 喔
## 心得
- CV 非我專長也
