```py
import random
import matplotlib.pyplot as plt

class SalemanMap:
    def __init__(self):
        self.x = []
        self.y = []
        self.names = []

    def set_names(self, names):
        self.names = names

    def get_map(self):
        for w in range(len(self.names)):
            self.x.append(random.randint(0, 100))
            self.y.append(random.randint(0, 100))

        plt.scatter(self.x, self.y)
        plt.xlabel("Distance (km)")
        plt.ylabel("Distance (km)")
        plt.xlim(0, 100)
        plt.ylim(0, 100)

        for i, name in enumerate(self.names):
            plt.text(self.x[i], self.y[i], name)  # Add name to the plot

        plt.show()

c = SalemanMap()
c.set_names(['Kobe', 'Gifu', 'Kobe', 'Tokyo'])
print(c.names)
c.get_map()
print(c.x)
```
<img width="1470" alt="Screenshot 2024-02-02 at 10 44 27" src="https://github.com/NaomiRozenberg/unit-3-/assets/142605919/75e25223-f1e1-40f3-8d9c-7d597ee14daf">


![IMG_FC2B59E43D7A-1](https://github.com/NaomiRozenberg/unit-3-/assets/142605919/999430a3-0b3a-45f7-b6ba-fdcfde395896)
