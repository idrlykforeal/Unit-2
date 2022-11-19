# Code
```.py
def getTruth():
    a=False
    b=False
    c=False
    count=0
    print("|DEC| A | B | C |")
    for i in range (8):
        dec=c+b*2+a*4
        print(f"| {dec} | {int(a)} | {int(b)} | {int(c)} |")
        c=not c
        count+=1
        if count%2==0:
            b=not b
        if count%4==0:
            a=not a

getTruth()
```

# Test
<img width="941" alt="Screen Shot 2022-10-31 at 1 51 22 PM" src="https://user-images.githubusercontent.com/100017195/198933591-19d0dc23-f32d-4f69-a897-3cb6782678c1.png">

# Truth table and circuit for:
Light = S1S2+(S2+S3(notS1))S1 

<img width="341" alt="Screen Shot 2022-11-19 at 2 17 30 PM" src="https://user-images.githubusercontent.com/100017195/202835606-8beea8d2-9c98-4400-bdea-4e1ea83cd09a.png">


![Untitled_Artwork 3](https://user-images.githubusercontent.com/100017195/202835729-08b96da4-35ad-4cd4-8ad4-2d273bf0634f.jpg)
