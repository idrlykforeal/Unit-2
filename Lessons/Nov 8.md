# Goal 1: count up
count in binary numbers with the lights following the following system diagram
<img width="899" alt="Screen Shot 2022-11-09 at 12 07 24 PM" src="https://user-images.githubusercontent.com/100017195/200728906-bfc5aeb4-4b6e-4f4c-b24d-21d8d37f43aa.png">

## How to get the location of the Arduino
ls / dev | grep cu

## Python code
```.py
from pyfirmata import Arduino
import time

board = Arduino('/dev/cu.usbserial-14230')
print("Communication Successfully started")

dig_12 = False
dig_9 = False
dig_5 = False
count = 0
binary=[]
for i in range(8):
    binary.append([dig_12, dig_9, dig_5])
    dig_5 = not dig_5
    count += 1
    if count % 2 == 0:
        dig_9 = not dig_9
    if count % 4 == 0:
        dig_12 = not dig_12

def light(dig_5, dig_9, dig_12):
    if dig_5==True:
        board.digital[5].write(1)
    if dig_9 == True:
        board.digital[9].write(1)
    if dig_12 == True:
        board.digital[12].write(1)
    time.sleep(1)
    board.digital[5].write(0)
    board.digital[9].write(0)
    board.digital[12].write(0)

for i in binary:
    light(i[2], i[1], i[0])
```

## Video
https://user-images.githubusercontent.com/100017195/200728998-35561904-1188-4177-bf07-662c56c8a0f2.MOV

# Goal 2: Display binary numbers
## Python code
```.py
from pyfirmata import Arduino
import time

def light(dig_5, dig_9, dig_12):
    if dig_5==True:
        board.digital[5].write(1)
    if dig_9 == True:
        board.digital[9].write(1)
    if dig_12 == True:
        board.digital[12].write(1)
    time.sleep(1)
    board.digital[5].write(0)
    board.digital[9].write(0)
    board.digital[12].write(0)

def validate_int_input(msg:str)->int:
    '''
    this function validates the user input of integers
    :param msg: str
    :return: int
    '''
    number=input(msg)
    while not number.isdigit():
        number = input( f'error, {msg}')
    return int(number)

board = Arduino('/dev/cu.usbserial-14230')
print("Communication Successfully started")

dig_12 = False
dig_9 = False
dig_5 = False
count = 0
binary=[]
for i in range(8):
    binary.append([dig_12, dig_9, dig_5])
    dig_5 = not dig_5
    count += 1
    if count % 2 == 0:
        dig_9 = not dig_9
    if count % 4 == 0:
        dig_12 = not dig_12


while True:
    number = validate_int_input("Please input a number between 0 and 7: ")
    while number < 0 or number > 7:
        number = validate_int_input("Invalid number, please input a number between 0 and 7: ")
    light(binary[number][2], binary[number][1], binary[number][0])
```

## Video
https://user-images.githubusercontent.com/100017195/201261137-72c30ea5-9b47-40b5-9395-90e46aa11806.mov
