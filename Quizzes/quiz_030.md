# Code

```.py
import matplotlib.pyplot as plt

h = [57.0, 56.0, 57.0, 56.0, 55.0, 55.0, 54.0, 54.0, 54.0, 53.0, 53.0, 54.0, 53.0, 53.0, 52.0, 52.0, 51.0, 51.0, 51.0, 50.0, 50.0, 49.0, 50.0, 49.0, 49.0, 48.0, 49.0, 49.0, 48.0, 48.0, 48.0, 49.0]

x=[]
y_smooth=[]
x_overlap=[]
y_overlap=[]
samples_per_window=4

for i in range (0, len(h), samples_per_window):
    data_in_window = h[i:i+samples_per_window]
    x.append(i)
    y_smooth.append(sum(data_in_window)/samples_per_window)

for i in range (0, len(h), int(samples_per_window*.5)):
    data_in_window = h[i:i+samples_per_window]
    x_overlap.append(i)
    y_overlap.append(sum(data_in_window)/samples_per_window)


plt.plot(x_overlap,y_overlap,"o-")
plt.ylabel('Relative humidity')
plt.xlabel('Samples')
plt.show()

```

# Graph plotted
<img width="560" alt="Screen Shot 2022-12-02 at 3 24 31 PM" src="https://user-images.githubusercontent.com/100017195/205229052-151387ed-c685-4c3d-87cc-ef5801e3d646.png">
