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
        y=2*(st+5)**2
        y_out.append(y)
        print("|"+f"{st:0.2f}".center(len)+"|"+f"{y:0.2f}".center(len)+"|")
        st += 0.2
    return x_out, y_out


data_x, data_y = produce()


from matplotlib import pyplot as plt
plt.plot(data_x, data_y, color="red", marker= '.')
plt.show()
```
# Plotted graph
<img width="344" alt="Screen Shot 2022-11-11 at 3 16 03 PM" src="https://user-images.githubusercontent.com/100017195/201275877-f309d4ec-bd9a-4c9e-8847-af34c323a3e4.png">


# Circuit for
not(bit0 bit1 + not (bit0 + bit1)) 

![Untitled_Artwork](https://user-images.githubusercontent.com/100017195/202834548-56f1ba2a-8b39-4b75-8e3a-1a9baefd06f2.jpg)
