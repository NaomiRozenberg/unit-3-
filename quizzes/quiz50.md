```py
class flight:
    def __init__(self, flight_num:str, origin:str, destination:str, departure_time:str, duration:list[int]):
        self.flight_num = flight_num
        self.origin = origin
        self.destination = destination
        self.departure_time = departure_time
        self.duration = duration
    def get_duration(self):
        return f"{self.duration[0]} hours {self.duration[1]} minutes {self.duration[2]} seconds"

object1 = flight(flight_num='AA123', origin='New York', destination='Los Angels', departure_time= "10:00 AM", duration=[5,30,3])

object2 = flight(flight_num='AA223', origin='New York', destination='Tokyo', departure_time= "11:00 PM", duration=[12,30,30])

print(object1.get_duration())
print(object2.get_duration())
```
<img width="1470" alt="Screenshot 2024-02-19 at 10 28 28" src="https://github.com/NaomiRozenberg/unit-3-/assets/142605919/f9cc80ea-2093-4249-9244-a0dc33452660">

![IMG_4EA3980E6B1E-1](https://github.com/NaomiRozenberg/unit-3-/assets/142605919/72d3c2f5-0077-4295-834f-841b09bfbbca)
