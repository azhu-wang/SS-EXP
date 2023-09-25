信號與系統實習
若想要在家中電腦執行以下程式，請前往 https://store.continuum.io/cshop/anaconda/ 下載Anaconda Python 軟體

實驗開始步驟：

(1)前往 https://github.com/htygithub/SS_EXP 點選右下角按鈕 "Download Zip"

(2)將 Zip 檔解壓縮至"我的文件"

(3)按下開始工具列->附屬應用程式->命令提示字元 來開啟命令列視窗

(4)於命令列鍵入 jupyter notebook 指令來開啟 Jupyter 視窗

(5)開啟Lesson_0_Scipy_intro.ipynb 開始以下實驗作答

實驗一: Numpy , Matplotlib 初見面
用滑鼠點選以下程式碼，並按下"Play"鈕執行看看結果

#coding: utf-8
%matplotlib inline
import numpy as np
import matplotlib.pyplot as plt
​
x=np.array([0,0,0,0,1,1,1,1,0,0,0,0])
plt.plot(x,'ro-')
[<matplotlib.lines.Line2D at 0x1f915a24b50>]

問題一
(1)按加號新增一個"Markdown"區塊，描述你看到了什麼。
(2)再按加號新增一個"code"區塊，嘗試畫出 "三個帽子"的波形
(按加號後，點選 'Cell Toolbar' 左方是下拉式選單，選擇 CODE)

(1)我看到了一個帽子波形

#coding: utf-8
%matplotlib inline
import numpy as np
import matplotlib.pyplot as plt
​
x=np.array([0,1,1,0,0,1,1,0,0,1,1,0])
plt.plot(x,'ro-')
#y=np.array([0,0,0,0,0,1,1,0])
#plt.plot(y,'bo-')
#z=np.array([0,0,0,0,0,0,0,0,0,1,1,0])
#plt.plot(z,'yo-')
[<matplotlib.lines.Line2D at 0x2bd84386490>]

實驗二: Python 之資料顯示以及np 陣列
用滑鼠點選以下程式碼，並按下"Play"鈕執行看看結果

#coding: utf-8
import numpy as np
​
t=np.arange(0,1,0.1)
print (t)
print ("這是 np.arange(0,1,0.1)的結果:" + str(t))
print ("加上一些換行字元\n\n\n" + "換行的結果是這樣\n")
t=np.arange(0,1,0.01)
print ("這是 np.arange(0,1,0.01)的結果:")
print (t)
sumt=sum(np.arange(0,10,1))
print ("\n\n\n這是 sum(np.arange(0,10,1))的結果:" +str(sumt))
[0.  0.1 0.2 0.3 0.4 0.5 0.6 0.7 0.8 0.9]
這是 np.arange(0,1,0.1)的結果:[0.  0.1 0.2 0.3 0.4 0.5 0.6 0.7 0.8 0.9]
加上一些換行字元


換行的結果是這樣

這是 np.arange(0,1,0.01)的結果:
[0.   0.01 0.02 0.03 0.04 0.05 0.06 0.07 0.08 0.09 0.1  0.11 0.12 0.13
 0.14 0.15 0.16 0.17 0.18 0.19 0.2  0.21 0.22 0.23 0.24 0.25 0.26 0.27
 0.28 0.29 0.3  0.31 0.32 0.33 0.34 0.35 0.36 0.37 0.38 0.39 0.4  0.41
 0.42 0.43 0.44 0.45 0.46 0.47 0.48 0.49 0.5  0.51 0.52 0.53 0.54 0.55
 0.56 0.57 0.58 0.59 0.6  0.61 0.62 0.63 0.64 0.65 0.66 0.67 0.68 0.69
 0.7  0.71 0.72 0.73 0.74 0.75 0.76 0.77 0.78 0.79 0.8  0.81 0.82 0.83
 0.84 0.85 0.86 0.87 0.88 0.89 0.9  0.91 0.92 0.93 0.94 0.95 0.96 0.97
 0.98 0.99]



這是 sum(np.arange(0,10,1))的結果:45
問題二
新增一個"Markdown"區塊，將以下問題之答案寫下來。
(1)請推論 np.arange 這個函數的用處，以及三個輸入值的意義。
(2)新增一個"code"區塊，利用python 程式碼，計算100以下偶數之總合。

(1)感覺是用來數數，有點像取樣，第一個是起始位置、第二個是結束位置、第三個是去樣區間，那他的程式是從0數到1，每個間隔0.1

#coding: utf-8
import numpy as np
​
print ("這是 np.arange(0,102,2)的結果:" + str(t))
sumt=sum(np.arange(0,102,2))
print ("\n\n\n這是100以下偶數之總合 sum(np.arange(0,102,2))的結果:" +str(sumt))
這是 np.arange(0,102,2)的結果:[  0   2   4   6   8  10  12  14  16  18  20  22  24  26  28  30  32  34
  36  38  40  42  44  46  48  50  52  54  56  58  60  62  64  66  68  70
  72  74  76  78  80  82  84  86  88  90  92  94  96  98 100]



這是100以下偶數之總合 sum(np.arange(0,102,2))的結果:2550
實驗三 : 弦波的頻率以及繪圖
用滑鼠點選以下程式碼，並按下"Play"鈕執行看看結果

#coding: utf-8
%matplotlib inline
import numpy as np
import matplotlib.pyplot as plt
​
t=np.arange(0,1,0.01)
pi=np.pi
curve=np.sin(2*pi*10*t)
curve2=np.sin(2*pi*5*t)
plt.plot(t,curve,'b',t,curve2,'r')
[<matplotlib.lines.Line2D at 0x1f915a4edd0>,
 <matplotlib.lines.Line2D at 0x1f915b19d90>]

問題三
(1)假設橫軸時間單位為秒，請問curve及curve2各為幾Hz弦波(也就是在一秒內走了幾個週期)？
(新增一個"Markdown"區塊，回答此問題)

(2)又我們如何改變指令，畫出一個 3 Hz的Cosine波呢？
(新增一個"CODE"區塊，回答此問題)

(1)curve為10Hz弦波/curve2為5Hz弦波

#coding: utf-8
%matplotlib inline
import numpy as np
import matplotlib.pyplot as plt
​
t=np.arange(0,1,0.01)
pi=np.pi
curve=np.cos(2*pi*3*t)
plt.plot(t,curve,'b')
[<matplotlib.lines.Line2D at 0x1f917b524d0>]

實驗四 : 影像以及RGB色彩
用滑鼠點選以下程式碼，並按下"Play"鈕執行看看結果

#coding: utf-8
%matplotlib inline
import numpy as np
import matplotlib.pyplot as plt
​
x=np.array([0,0,0,1,1,1,1,0,0,0])
y=np.array([x,x,x,x,x,x,x,x,x,x])
print(y)
print(y.shape)
plt.figure(1)
plt.imshow(y,cmap='gray',interpolation='nearest')
y=np.array([x/5.,x/4.,x/3.,x/2.,x/1.,x,x,x,x,x])
plt.figure(2)
plt.imshow(y,cmap='gray',interpolation='nearest')
[[0 0 0 1 1 1 1 0 0 0]
 [0 0 0 1 1 1 1 0 0 0]
 [0 0 0 1 1 1 1 0 0 0]
 [0 0 0 1 1 1 1 0 0 0]
 [0 0 0 1 1 1 1 0 0 0]
 [0 0 0 1 1 1 1 0 0 0]
 [0 0 0 1 1 1 1 0 0 0]
 [0 0 0 1 1 1 1 0 0 0]
 [0 0 0 1 1 1 1 0 0 0]
 [0 0 0 1 1 1 1 0 0 0]]
(10, 10)
<matplotlib.image.AxesImage at 0x2bdfdd851d0>


問題四
(1)請問y 矩陣的大小為何？
(2)試完成一個10x10的矩陣，顯示一個白色十字。 (新增一個"CODE"區塊，回答此問題)

(1)10x10

#coding: utf-8
%matplotlib inline
import numpy as np
import matplotlib.pyplot as plt
​
x=np.array([0,0,0,1,1,1,1,0,0,0])
z=np.array([1,1,1,1,1,1,1,1,1,1])
y=np.array([x,x,x,z,z,z,z,x,x,x])
print(y)
print(y.shape)
plt.figure(1)
plt.imshow(y,cmap='gray',interpolation='nearest')
y=np.array([x/5.,x/4.,x/3.,x/2.,x/1.,x,x,x,x,x])
​
[[0 0 0 1 1 1 1 0 0 0]
 [0 0 0 1 1 1 1 0 0 0]
 [0 0 0 1 1 1 1 0 0 0]
 [1 1 1 1 1 1 1 1 1 1]
 [1 1 1 1 1 1 1 1 1 1]
 [1 1 1 1 1 1 1 1 1 1]
 [1 1 1 1 1 1 1 1 1 1]
 [0 0 0 1 1 1 1 0 0 0]
 [0 0 0 1 1 1 1 0 0 0]
 [0 0 0 1 1 1 1 0 0 0]]
(10, 10)

實驗五 :RGB色彩
用滑鼠點選以下程式碼，並按下"Play"鈕執行看看結果

#coding: utf-8
%matplotlib inline
import numpy as np
import matplotlib.pyplot as plt
​
x=np.array([0,0,0,1,1,1,1,0,0,0])
y=np.array([x,x,x,x,x,x,x,x,x,x])
z=np.zeros([10,10,3])
z[:,:,0]=y 
plt.figure(figsize=[15,5])
plt.subplot(1,4,1)
plt.imshow(z,interpolation='nearest')
#######################################
z=np.zeros([10,10,3])
z[:,:,1]=y
plt.subplot(1,4,2)
plt.imshow(z,interpolation='nearest')
#######################################
z=np.zeros([10,10,3])
z[:,:,2]=y
plt.subplot(1,4,3)
plt.imshow(z,interpolation='nearest')
#######################################
z=np.zeros([10,10,3])
z[:,:,0]=y
z[:,:,1]=y
plt.subplot(1,4,4)
plt.imshow(z,interpolation='nearest')
<matplotlib.image.AxesImage at 0x1f915b64c10>

問題五
以上範例是將紅光、綠光、藍光分別開至最大亮度 (數值1)
若是將紅、綠、藍分別以1, 0.5, 0 來表示, 試著新增一組程式碼完成配色，並說明合成的顏色為？

import numpy as np
import matplotlib.pyplot as plt
​
# 创建红光、绿光、蓝光分量的数组
red_channel = np.array([0, 1, 1, 1, 1, 1, 1, 1, 1, 0])
green_channel = np.array([0, 0.5, 0.5, 0.5, 0.5, 0.5, 0.5, 0.5, 0.5, 0])
blue_channel = np.array([0, 0, 0, 0, 0, 0, 0, 0, 0, 0])
​
# 创建彩色图像
color_image = np.zeros([10, 10, 3])
color_image[:, :, 0] = red_channel
color_image[:, :, 1] = green_channel
color_image[:, :, 2] = blue_channel
​
# 绘制图像
plt.imshow(color_image, interpolation='nearest')
plt.show()
