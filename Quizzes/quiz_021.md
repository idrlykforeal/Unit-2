# Code

```.py
def getTruth():
    a=False
    b=False
    c=False
    count=0
    truth=" AB + not B + not B C "
    print(f"|DEC| A | B | C |{truth}|")
    for i in range (8):
        dec=c+b*2+a*4
        ans= (a and b) or (not b) or ((not b) and c)
        print(f"| {dec} | {int(a)} | {int(b)} | {int(c)} |" + f"{int(ans)}".center(len(truth))+ "|")
        c=not c
        count+=1
        if count%2==0:
            b=not b
        if count%4==0:
            a=not a

getTruth()

```

# Test 
<img width="938" alt="Screen Shot 2022-11-03 at 8 22 20 AM" src="https://user-images.githubusercontent.com/100017195/199620576-99c6acae-8a8c-4a41-b770-0d31783f2365.png">

# Truth table and circuit for:
X = ZW ⨁ (Z ⨁ Y(not W)) 

![Untitled_Artwork 2](https://user-images.githubusercontent.com/100017195/202835026-562b9221-a439-40a7-a541-3c1ff816c700.jpg)

<img width="308" alt="Screen Shot 2022-11-19 at 2 12 42 PM" src="https://user-images.githubusercontent.com/100017195/202835482-ed34a0c6-cec5-4205-9acf-00597d4422bf.png">
