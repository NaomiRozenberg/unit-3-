```py
class Converter:
    def __init__(self):
        self.roman_numbers = {
            100: 'C', 90: 'XC', 50: 'L', 40: 'XL', 10: 'X', 9: 'IX', 5: 'V', 4: 'IV', 1: 'I'
        }

    def convert_to_roman(self, decimal):
        if 0 < decimal <= 100:
            output = ''
            for dec, roman in self.roman_numbers.items():
                quotient, decimal = divmod(decimal, dec)
                output += roman * quotient
            return output
        else:
            return "Please enter a number between 1 and 100."

converter = Converter()
print(converter.convert_to_roman(45))

```
<img width="1470" alt="Screenshot 2024-02-01 at 10 00 54" src="https://github.com/NaomiRozenberg/unit-3-/assets/142605919/9d1eb3b2-1373-44c7-a6fb-a9eededa3859">
![JPEG image-4A9A-9316-4A-0](https://github.com/NaomiRozenberg/unit-3-/assets/142605919/5dee979c-93e2-47c1-a527-af68d2b9e6d4)
