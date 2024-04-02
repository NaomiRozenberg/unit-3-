```py
class Flight:
    def __init__(self, flight_num: str, origin: str, destination: str, departure_time: str, duration: list[int]):
        self.flight_num = flight_num
        self.origin = origin
        self.destination = destination
        self.departure_time = departure_time
        self.duration = duration

    def get_duration(self):
        return f"{self.duration[0]} hours {self.duration[1]} minutes {self.duration[2]} seconds"


class Aircraft(Flight):
    def __init__(self, flight_num: str, origin: str, destination: str, departure_time: str, duration: list[int], model: str, capacity: int):
        super().__init__(flight_num, origin, destination, departure_time, duration)
        self.model = model
        self.capacity = capacity

    def get_info(self):
        return f"Flight {self.flight_num} from {self.origin} to {self.destination} departs at {self.departure_time}. Aircraft: {self.model} (Capacity: {self.capacity})"



objectFlt = Flight('AA123', 'New York', 'Los Angeles', '10:00 AM', [5, 30, 0])
objectAir = Aircraft('AA123', 'New York', 'Los Angeles', '10:00 AM', [5, 30, 0],'BOeing 737', 150)


def print_object_info(obj, method_name):
    if hasattr(obj, method_name):
        method = getattr(obj, method_name)
        if callable(method):
            result = method()
            print(result)
            return result
    return f"Method {method_name} not found or not callable."


print_object_info(objectFlt, 'get_duration')
print_object_info(objectAir, 'get_info')
```
<img width="1470" alt="Screenshot 2024-04-01 at 12 11 28" src="https://github.com/NaomiRozenberg/unit-3-/assets/142605919/6addae49-4c87-43d9-a261-dd93a3f8e7cb">
![Uploading JPEG image-43F0-BEA9-B8-0.jpeg…]()
