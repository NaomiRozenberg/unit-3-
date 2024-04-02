```py
import math


class Wheel:
    def __init__(self, size: int):
        self.size = size
        self.count = 0
        self.km = 0

    def get_size(self):
        return f"The wheel size is {self.size} (Inches)"

    def get_perimeter(self):
        return math.pi * self.size * 2

    def km_per_rotation(self):
        while self.km < 1000:
            self.km += self.size
            self.count += 1


class Bicycle:
    def __init__(self, wheel: Wheel, frame_material: str):
        self.wheel = wheel
        self.frame_material = frame_material

    def ride(self):
        print(f'The wheel size: {self.wheel.get_size()}. The frame material: {self.frame_material}')


bicycle = Bicycle(Wheel(26), 'aluminum')

bicycle.ride()

km_per_rotation = bicycle.wheel.get_perimeter() / 1000  
print(f"Distance traveled in kilometers per rotation: {km_per_rotation} km")
```
<img width="1470" alt="Screenshot 2024-04-01 at 12 54 24" src="https://github.com/NaomiRozenberg/unit-3-/assets/142605919/e093ceb3-0bd0-473b-87e0-06307b000cd2">
![IMG_5D7122D1AACD-1](https://github.com/NaomiRozenberg/unit-3-/assets/142605919/45a53e64-f4ae-45a8-abaa-7c2ed307231c)
