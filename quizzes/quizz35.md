```py 
def mystery(list1, list2):
    output = []
    for x in list1:
        for y in list2:
            if x == y:
                output.append(x)
    return output
list1 = [2,3,4,5,6,1]
list2 = [2,4,5,6,2,0]
test1= mystery(list1,list2)
print(test1)
```
<img width="1470" alt="Screenshot 2024-02-01 at 9 48 35" src="https://github.com/NaomiRozenberg/unit-3-/assets/142605919/0fc8bd47-9dc8-42e2-b0b4-c8a49c6efee1">
