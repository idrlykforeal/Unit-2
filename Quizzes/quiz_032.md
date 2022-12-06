# Code
```.py
import requests
import matplotlib.pyplot as plt
import numpy as np
req=requests.get('http://192.168.6.142/readings')
readings=req.json()['readings']
readings=readings[0]

data_9=[]
data_10=[]

for i in readings:
    if i['sensor_id']==9: # humidity sensor
        data_9.append(i['value'])

for i in readings:
    if i['sensor_id']==10: # temperature sensor
        data_10.append(i['value'])

#smoothing data of 12 samples
data_9_smooth=[]
data_10_smooth=[]

for i in range(0,len(data_9),12):
    data_in_window=data_9[i:i+12]
    average_9=sum(data_in_window)/12
    data_9_smooth.append(average_9)
for i in range(0,len(data_10),12):
    data_in_window=data_10[i:i+12]
    average_10=sum(data_in_window)/12
    data_10_smooth.append(average_10)


x=[]
for i in range(45):
    x.append(i+1)

#plotting the data
plt.subplot(3,1,1)
plt.plot(x,data_9_smooth[0:45])
plt.subplot(3,1,2)
plt.plot(x,data_10_smooth[0:45])


diff=[]

for i in range(len(data_9_smooth)):
    d=data_9_smooth[i]-data_10_smooth[i]
    diff.append(d)

plt.subplot(3,1,3)
plt.plot(diff[0:45])
plt.show()
```

# Graphs plotted
<img width="453" alt="Screen Shot 2022-12-06 at 1 48 50 PM" src="https://user-images.githubusercontent.com/100017195/205818476-2511c49d-35af-4ecb-a628-7e888ee801c8.png">

# What are three main operators used in boolean logic?
- and
- or 
- not
