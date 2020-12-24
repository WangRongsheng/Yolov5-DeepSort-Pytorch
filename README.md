# 一、实时目标跟踪检测

> 原项目地址：https://github.com/mikel-brostrom/Yolov5_DeepSort_Pytorch


![](Town.gif)

# 二、准备

## 1、配置环境

- `Python 3.8`
- `pip install -U -r requirements.txt`
- `torch> = 1.6`

## 2、克隆项目
```html
git clone --recurse-submodules https://github.com/mikel-brostrom/Yolov5_DeepSort_Pytorch.git
```

如果你下载好了仓库并且没有使用`--recurse-submodules`，则可以运行`git submodule update --init` 

## 3、下载权重

- 从最新的Realease https://github.com/ultralytics/yolov5/releases 下载yolov5权重。将下载后的`.pt文件`放在`yolov5/weights/`
- 从 https://drive.google.com/drive/folders/1xhG0kRH1EX5B9_Iz8gQJb7UNnn_riXi6 下载深度排序权重。将`ckpt.t7`文件放在`deep_sort/deep/checkpoint/`

> 全部权重下载：[百度网盘下载权重文件（提取码：9hff）](https://pan.baidu.com/s/1Nt4GU0QH9VU9AkQ-JIsflg)
 


## 三、运行
```html
python3 track.py --source ...
```

- 视频： --source file.mp4
- 摄像头： --source 0
- RTSP流： --source rtsp://170.93.143.139/rtplive/470011e600ef003a004ee33696235daa
- HTTP流： --source http://wmccpinetop.axiscam.net/mjpg/video.mjpg

结果可以保存到`inference/output`：

```html
python3 track.py --source ... --save-txt
```

# 三、参考

- https://xugaoxiang.com/2020/10/17/yolov5-deepsort-pytorch/
- https://www.bilibili.com/video/BV1cp4y1k7xd/





