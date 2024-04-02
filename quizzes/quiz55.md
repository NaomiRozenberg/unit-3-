```py
import math


class Darts:
    def __init__(self, x, y):
        self.x = x
        self.y = y

    def calculate_points(self):
        distance_from_center = math.sqrt(self.x ** 2 + self.y ** 2)

        if distance_from_center > 10:
            return 0
        elif distance_from_center > 5:
            return 1
        elif distance_from_center > 1:
            return 5
        else:
            return 10

dart1 = Darts(7, 7)
print("Points earned for dart at coordinates (7, 7):", dart1.calculate_points())
```
<img width="1470" alt="Screenshot 2024-04-02 at 23 57 31" src="https://github.com/NaomiRozenberg/unit-3-/assets/142605919/9315500b-556f-4f67-901c-5b938a58500a">
![IMG_1C89022F9A46-1](https://github.com/NaomiRozenberg/unit-3-/assets/142605919/8cc9e993-28b0-43be-b304-eb7fdf4de63c)
