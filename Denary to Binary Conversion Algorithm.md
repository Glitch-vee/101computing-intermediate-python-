
In this challenge, we are going to write an algorithm to convert a decimal (aka Denary) number between 0 and 255 into binary using 1 Byte (=8 bits).

Now, let's write the program using the basics.
```python
denary= int(input("Enter a number between 0 and 255:   "))

if denary>=0 and denary<=255:
    binary = ""
    if denary>=128:
        binary = binary + "1"
        denary = denary - 128
    else:
        binary = binary + "0"
    if denary>=64:
        binary = binary + "1"
        denary = denary - 64
    else:
        binary = binary + "0"
    if denary>=64:
        binary = binary + "1"
        denary = denary - 64
    else:
        binary = binary + "0"
    if denary>=32:
        binary = binary + "1"
        denary = denary - 32
    else:
        binary = binary + "0"
    if denary>=16:
        binary = binary + "1"
        denary = denary - 16
    else:
        binary = binary + "0"
    if denary>=8:
        binary = binary + "1"
        denary = denary - 8
    else:
        binary = binary + "0"
    if denary>=4:
        binary = binary + "1"
        denary = denary - 4
    else:
        binary = binary + "0"
    if denary>=2:
        binary = binary + "1"
        denary = denary - 2
    else:
        binary = binary + "0"
    if denary>=1:
        binary = binary + "1"
        denary = denary - 1
    else:
        binary = binary + "0"
    
    print(binary)
    
    
else:
    print("Invalid number")
```

Above we have done the coding in elementary way. We can use function to make it more simple and also a code to validate the input so that your code only accepts a number between 0 and 255
Let's make a function called, convertToBinary(). This function will take a denary number as a parameter and return a binary string. ​




```python
x= int(input( "Enter a number between 0 to 255:   "))

def convertToBinary(denary):
    binary = ""
    bits = [128, 64, 32, 16, 8, 4, 2, 1]
    
    if denary>=0 and denary<=255:
        for bit in bits:
            if denary >= bit:
                binary += "1"
                denary -= bit
            else:
                binary += "0"
        return binary

    else:
        print("Invalid number")
        
print(convertToBinary(x))
```
