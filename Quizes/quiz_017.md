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
