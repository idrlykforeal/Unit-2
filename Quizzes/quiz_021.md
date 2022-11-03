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
