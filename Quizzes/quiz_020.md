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
