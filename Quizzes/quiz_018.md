# Code
## Math equation method
```.py
from math import ceil

def numberMatches(l:int, s:int)->int:
    mps=s/100
    num_matches=ceil(l/(mps*5))
    return num_matches

out=numberMatches(l=100, s=100)
print(out)

out=numberMatches(l=250, s=110)
print(out)

out=numberMatches(l=500, s=150)
print(out)

out=numberMatches(l=12345, s=123)
print(out)
```

## while loop function
```.py
def numberMatches(l:int, s:int)->int:
    lyli_position=0
    speed_mps=s/100
    seconds_passed=0
    matches=0
    while lily_position<1:
        seconds_passed+=1
        #move lili
        lili_position+=speed_mps
        if seconds_passed == 5:
            matches+=1
            print(f"A match is lit")
            seconds_passed=0
    return matches
```
### Flow diagram
![Comp Science](https://user-images.githubusercontent.com/100017195/197921767-94516d46-e5b6-4d13-9d01-f7919d0bf877.jpeg)

# Test
<img width="978" alt="Screen Shot 2022-10-26 at 11 24 48 AM" src="https://user-images.githubusercontent.com/100017195/197919780-dcb35e40-6122-4d1d-ab27-3309258023ad.png">

# Truth table
for out=ABC+(A+B+C)+not(notA notB notC)

| A | B | C | out |
|---|---|---|---|
| 0 | 0 | 0 | 0 |
| 0 | 0 | 1 | 1 |
| 0 | 1 | 0 | 1 |
| 0 | 1 | 1 | 1 |
| 1 | 0 | 0 | 1 |
| 1 | 0 | 1 | 1 |
| 1 | 1 | 0 | 1 |
| 1 | 1 | 1 | 1 |
