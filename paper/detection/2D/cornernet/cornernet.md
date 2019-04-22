## 简介
论文是ECCV2018的第一篇文章，第一次提取利用keypoint的检测的思路解决2D 物体检测问题。开物体检测小方向。

## 关键思想
1. 通过预测物体左上和右下的点来预测物体的位置，和anchor-based的single-stage、two-stage的方法思路不同。属于anchor-free方法。
2. 为了更好的预测物体左上和右下的坐标点，提出corner pooling，充分利用物体的左右边框信息。
![cmd-markdown-logo](https://github.com/ZhipengLiu6/image_cloud/raw/master/paper/detection/2D/cornernet/pipline.JPG)
## 算法流程
示意图如图所示:
### input
1. 图片
### output
1. 物体左上和右下的关键点的heatmap, C x W X H, C表示物体类别的个数。
2. 物体左上和右下两对点的关联信息，embeddings，维度信息需要看代码获取。
3. 物体左上关键点的位移修正信息（由于下采样会损失位置信息），维度信息需要阅读代码获取。
### 详细过程
1. 经过hourglass network

## 代码解读：

## **参考**
1. https://zhuanlan.zhihu.com/p/41825737
