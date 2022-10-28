# Code
```.py
def get_l3tt3r(msg:str)->str:
    out=""
    for i in msg:
        if i==" ":
            out+="_"
        elif i=="a":
            out+="4"
        elif i=="e":
            out+="3"
        elif i=="i":
            out+="1"
        elif i=="o":
            out+="0"
        else:
            out+=i
    return out

print(get_l3tt3r("Hello World"))
print(get_l3tt3r("Why did I chose CS?"))
print(get_l3tt3r("Remember the Figure Caption"))
```

# Test
<img width="941" alt="19" src="https://user-images.githubusercontent.com/100017195/198516336-ccdee2a7-584b-48de-8090-771c57fcecb9.png">
