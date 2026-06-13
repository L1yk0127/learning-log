# 图像预处理笔记

## 图像读取

```python
import cv2
img = cv2.imread('path/to/image.jpg')
# 注意：OpenCV 读入是 BGR 顺序，不是 RGB
```

## 颜色空间转换

```python
gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)   # 转灰度
rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)     # 转 RGB（plt 显示用）
hsv = cv2.cvtColor(img, cv2.COLOR_BGR2HSV)     # 转 HSV
```

## 图像尺寸操作

```python
h, w, c = img.shape                           # 获取尺寸
resized = cv2.resize(img, (256, 256))          # 缩放
cropped = img[50:200, 100:300]                # 裁剪
```

## 画图

```python
cv2.rectangle(img, (x1,y1), (x2,y2), (0,255,0), 2)   # 矩形
cv2.circle(img, (cx,cy), r, (0,0,255), -1)            # 圆形
cv2.putText(img, 'hello', (x,y), font, 1, (255,255,255), 2)  # 文字
```
