```py
class palNum:
    def __init__(self, A, B):
        self.A = A
        self.B = B

    @staticmethod
    def is_palindrome(num):
        return str(num) == str(num)[::-1]

    def get_pal_list(self):
        palindromes = []
        for num in range(self.A, self.B + 1):
            if self.is_palindrome(num):
                palindromes.append(num)
        return palindromes

A = 10
B = 199
obj = palNum(A, B)
palindrome_list = obj.get_pal_list()
print(palindrome_list)
```

<img width="1470" alt="Screenshot 2024-04-01 at 13 19 12" src="https://github.com/NaomiRozenberg/unit-3-/assets/142605919/7501fcf2-256d-4477-bbfe-fb81d158cb93">
![IMG_6BFA44797CFE-1](https://github.com/NaomiRozenberg/unit-3-/assets/142605919/81a93a33-8e35-4155-bab5-18c3bb1595e5)
