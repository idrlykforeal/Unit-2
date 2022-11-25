# Code
```.py
from matplotlib import pyplot as plt
import numpy as np

sensorA = [16, 24, 24, 9, 23, 26, 26, 23, 25, 14]
sensorB = [2, 19, 25, 10, 11, 24, 17, 7, 24, 17]
sensorC = [15, 11, 24, 21, 6, 2, 18, 27, 1, 16]

sample=[]

for i in range(len(sensorA)):
    sample.append(i+1)

fig= plt.figure(figsize=(15,6))
plt.subplot(1,2,1)
plt.plot(sample, sensorA)
plt.plot(sample, sensorB)
plt.plot(sample, sensorC)


mean=[]
stad=[]

for i in range(len(sensorA)):
    data = [sensorA[i], sensorB[i], sensorC[i]]
    mean.append(np.mean(data))
    stad.append(np.std(data))

plt.subplot(1,2,2)
plt.plot(sample, mean)
plt.errorbar(sample, mean,stad, fmt="o", color="black")
plt.show()
```
# Outcome

<img width="799" alt="Screen Shot 2022-11-25 at 3 49 17 PM" src="https://user-images.githubusercontent.com/100017195/203917893-58c74b5d-8f1e-4d87-86ea-b1f2bae5ee2b.png">

# Convert the following rgb color to hex color 
red=250, green=100, blue=10
red = FA

| Division | Quotient | Remainder(Digit) | Digit # |
|----------|----------|------------------|---------|
| 250/16   | 15       | 10               | 0       |
| 15/16    | 0        | 15               | 1       |

green = 64

| Division | Quotient | Remainder(Digit) | Digit # |
|----------|----------|------------------|---------|
| 100/16   | 6        | 4                | 0       |
| 6/16     | 0        | 6                | 1       |

blue = 0A

| Division | Quotient | Remainder(Digit) | Digit # |
|----------|----------|------------------|---------|
| 10/16    | 0        | 10               | 0       |
| 6/16     | 0        | 6                | 1       |

Hex color= FA640A
