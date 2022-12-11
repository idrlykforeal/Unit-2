# Code
```.py
from matplotlib.gridspec import GridSpec

def get_sensor(readings: list, id: int) -> list:
    data = []
    for i in readings:
        if i['sensor_id'] == id:
            data.append(i['value'])
    return data
def download_data(url:str="192.168.6.142/readings")->list:
    req = requests.get(f"http://{url}")
    readings=req.json()['readings'][0]
    return readings
def smoothing(data:list,size_window:int=12):
    data_smooth=[]
    for i in range(0,len(data),size_window):
        data_in_window=data[i:i+size_window]
        average=sum(data_in_window)/size_window
        data_smooth.append(average)
    return data_smooth


import requests
import matplotlib.pyplot as plt
import numpy as np
readings=download_data()
sensors=[6,8,9,10]

data_6=[]
data_8=[]
data_9=[]
data_10=[]


data_6=get_sensor(readings,6)
data_8=get_sensor(readings,8)
data_9=get_sensor(readings,9)
data_10=get_sensor(readings,10)


data_6=data_6[0:499]
data_8=data_8[0:499]
data_9=data_9[0:499]
data_10=data_10[0:499]

#average of 4 sensors
average=[]
for i in range(0,499):
    average.append((data_6[i]+data_8[i]+data_9[i]+data_10[i])/4)

#smoothing data of 12 samples
data_6_smooth=smoothing(data_6,10)
data_8_smooth=smoothing(data_8,10)
data_9_smooth=smoothing(data_9,10)
data_10_smooth=smoothing(data_10,10)
average_smooth=smoothing(average,10)

#plotting the data
# style of graph
plt.style.use('seaborn-whitegrid')
fig=plt.figure(figsize=(10,8))
grid=GridSpec(4,4,figure=fig)
#create big plot
box1=fig.add_subplot(grid[0:4,0:3])
plt.plot(average_smooth)
plt.title("Smoothed average of 4 sensors")
plt.xlabel("Time")
plt.ylabel("Temperature in Celsius")

datas=[data_6_smooth,data_8_smooth,data_9_smooth,data_10_smooth]

#create small plots
for i in range(len(sensors)):
    box=fig.add_subplot(grid[i,3])
    plt.plot(datas[1])
    plt.title(f"Sensor {sensors[i]}")
    plt.xlabel("Time")
    plt.ylabel("Temperature in Celsius")
plt.show()
```
# Graph plotted
![4+1_data](https://user-images.githubusercontent.com/100017195/206909523-a8805c9a-a879-4664-8479-61f0f94e49fc.jpeg)
