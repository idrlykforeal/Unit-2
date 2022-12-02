# Code
```.py

t1=610
t2=800

import requests
import numpy as np
import matplotlib.pyplot as plt

req=requests.get("http://192.168.6.142/readings")
data=req.json()

readings=data["readings"][0]

tempreature=[]
temp_index=[]

a=1

for i in readings:
    if i["sensor_id"]==1:
        tempreature.append(i["value"])
        temp_index.append(a)
        a+=1

selected_temp=tempreature[t1:t2]
selected_index=temp_index[t1:t2]

#plot the selected data
plt.scatter(selected_index,selected_temp)

#calculate and plot the line of best fit
k,j=np.polyfit(selected_index,selected_temp,1) #k is the gradient and j is the y intercept
index=[610,800]
y=[k*610+j,k*800+j]
plt.plot(index,y)

#calculate and plot a quadratic fit
m,b,c=np.polyfit(selected_index,selected_temp,2)
y=[]
for i in selected_index:
    y.append(m*i**2+b*i+c)
plt.plot(selected_index,y)

plt.show()

```

# Graph plotted
<img width="560" alt="Screen Shot 2022-12-02 at 3 23 09 PM" src="https://user-images.githubusercontent.com/100017195/205228854-acaa26e5-3d2b-40ea-acd3-abef9fa2ffe7.png">
