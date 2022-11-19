```.py
import random
random.seed(1234)

def produce(n: int, m:int, s:int) -> float:
    len=15
    x_out=[]
    y_out=[]
    print("|"+f"x".center(len)+"|"+f"y".center(len)+"|\n")
    for i in range(n):
        x = random.randint(0, 100)
        x_out.append(x)
        y=x**(1/2*(m/s)**2)
        y_out.append(y)
        print("|"+f"{x}".center(len)+"|"+f"{y:0.2f}".center(len)+"|\n")
    return x_out, y_out

from matplotlib import pyplot as plt

data_x, data_y = produce(10, 3, 2)

plt.plot(data_x, data_y, color="red", marker= '.')
plt.show()
```

<img width="364" alt="Screen Shot 2022-11-11 at 3 03 52 PM" src="https://user-images.githubusercontent.com/100017195/201274308-e4eee66d-bd72-453a-a6e1-f38c656550a7.png">

# Truth table

<img width="123" alt="Screen Shot 2022-11-19 at 1 45 55 PM" src="https://user-images.githubusercontent.com/100017195/202834581-b6d33614-dc05-4ee5-9880-ef60a3e29c8e.png">

| A | B | A(A xor B) |
|---|---|------------|
| 0 | 0 | 0          |
| 0 | 1 | 0          |
| 1 | 0 | 1          |
| 1 | 1 | 0          |
