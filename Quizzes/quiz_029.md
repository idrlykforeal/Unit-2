# Code
```.py
def Count_letters(lexicon:dict,msg:str)->dict:
    for letter in msg:
        if letter in lexicon.keys():
            lexicon[letter]+=1
    return lexicon


my_dict = {'w':0,'l':0,"c":0}
msg = "hello world"

print(Count_letters(my_dict,msg))

my_dict = {'a':0, 'e':0, 'i':0, 'o':0, 'u':0 }
msg = "Why did i choose CS"

print(Count_letters(my_dict,msg))
```

# Test results
<img width="923" alt="Screen Shot 2022-11-24 at 8 19 26 AM" src="https://user-images.githubusercontent.com/100017195/203662285-f328cd38-392e-4c8f-b5dc-df1cb3ce1dfd.png">

# How many different colors could you represent in a 6 bit computer? 
2^6=64
