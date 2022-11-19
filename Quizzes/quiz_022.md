# Code
```.py
import random
random.seed(1234)

def produce(n: int, m:int, s:int) -> float:
    len=15
    out_print="|"+f"x".center(len)+"|"+f"y".center(len)+"|\n"
    for i in range(n):
        x = random.randint(0, 100)
        y=x**(1/2*(m/s)**2)
        out_print+="|"+f"{x}".center(len)+"|"+f"{y:0.2f}".center(len)+"|\n"
    return out_print

sample=produce(5, 3, 2)
print(sample)

```

# Test

<img width="942" alt="Screen Shot 2022-11-08 at 1 35 27 PM" src="https://user-images.githubusercontent.com/100017195/200476008-94f27cf9-2f3c-42c1-9c0d-d03504f3ab16.png">

# Proof that :
A (A + B) = A 

| A | B | A(A+B) |
|---|---|--------|
| 0 | 0 | 0      |
| 0 | 1 | 0      |
| 1 | 0 | 1      |
| 1 | 1 | 1      |
