# Goal
Create a function that produces the average word length of the input list.

# code

```.py
def averageLength(l:list)->float:
    s=0
    count=0
    for i in l:
        s+=len(i)
        count+=1
    return s/count

givenlist=["hello","main"]
print(averageLength(givenlist))

givenlist=["Peru","France", "Nepal"]
print(averageLength(givenlist))

givenlist=["Computer","Science", "Art"]
print(averageLength(givenlist))

givenlist=["one","two"]
print(averageLength(givenlist))

```

# Test
![17](https://user-images.githubusercontent.com/100017195/198516490-b7897422-d7b5-493b-a496-a7961f4f2ab8.jpg)
