```py
class rainDrops:
    def __init__(self, n: int):
        self.n = n
        self.out = ''
        self.list = []
        self.notList = []

    def pour(self):
        if self.n % 3 == 0:
            self.out += 'Pling'
        if self.n % 5 == 0:
            self.out += 'Plang'
        if self.n % 7 == 0:
            self.out += 'Plong'

        if not self.out:
            self.out = str(self.n)
            print(f'{self.n} is not divisible by 3, 5, or 7, so the result would be "{self.out}"')
        else:
            if 'Pling' in self.out:
                self.list.append(3)
            if 'Plang' in self.out:
                self.list.append(5)
            if 'Plong' in self.out:
                self.list.append(7)

            if 'Pling' not in self.out:
                self.notList.append(3)
            if 'Plang' not in self.out:
                self.notList.append(5)
            if 'Plong' not in self.out:
                self.notList.append(7)

            print(f'{self.n} is divisible by {self.list} but not by {self.notList}, the result is {self.out}')


rainDrops(30).pour()

```
![Uploading Screenshot 2024-04-01 at 13.44.20.png…]()

![IMG_65FE691109BE-1](https://github.com/NaomiRozenberg/unit-3-/assets/142605919/3dbda58a-acd7-4c29-b4f8-36f79adbcf5b)
