# Code
```.py
def produce():
    st = -10
    len=10
    x_out=[]
    y_out=[]
    print("|"+f"x".center(len)+"|"+f"y".center(len)+"|\n")
    for i in range(101):
        x_out.append(st)
        y=abs(st)
        y_out.append(y)
        print("|"+f"{st:0.2f}".center(len)+"|"+f"{y:0.2f}".center(len)+"|")
        st += 0.2
    return x_out, y_out

data_x, data_y = produce()
from matplotlib import pyplot as plt
plt.plot(data_x, data_y, color="red", marker= '.')
plt.show()
```

# Graph plotted
<img width="433" alt="Screen Shot 2022-11-15 at 1 25 30 PM" src="https://user-images.githubusercontent.com/100017195/201826096-65829dc8-4de6-482a-9c7a-82479f4e362a.png">

# Base conversion:
FFA5 (base 16) to decimal:

(FFA5)16 = (15 × 16^3) + (15 × 16^2) + (10 × 16^1) + (5 × 16^0) = (65445)10
