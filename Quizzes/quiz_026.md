# Code
```.py
from matplotlib import pyplot as plt
import numpy as np

len =10
x =[]
h = [57.0, 56.0, 57.0, 56.0, 55.0, 55.0, 54.0, 54.0, 54.0, 53.0, 53.0, 54.0, 53.0, 53.0, 52.0, 52.0, 51.0, 51.0,
         51.0, 50.0, 50.0, 49.0, 50.0, 49.0, 49.0, 48.0, 49.0, 49.0, 48.0, 48.0, 48.0, 49.0]

for i in range(32):
    x.append( i +1)
    print("| " +f"{ i +1}".center(len ) +"| " +f"{h[i]:0.2f}".center(len ) +"|")


m,b = np.polyfit(x,h,1)

plt.xlabel("samples")
plt.ylabel("humidity")
plt.scatter(x, h, color="green", marker= '.')
linex=[0,32]
liney=[m*0+b,m*32+b]
plt.plot(linex,liney,"r")
plt.show()
```

# Graph plotted

<img width="527" alt="Screen Shot 2022-11-16 at 11 48 13 AM" src="https://user-images.githubusercontent.com/100017195/202071537-e7af64a2-1a25-4425-9057-36ffbe9ac334.png">

# Convert color in hex to rgb
#e6e627

(e6)16=(230)2

(e6)16=(230)2

(27)16=(39)2

rgb(230, 230, 39)
