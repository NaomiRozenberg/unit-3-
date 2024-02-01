``` py
from kivymd.app import MDApp
class quiz39(MDApp):
    def __init__(self, **kwargs):
        super().__init__(**kwargs)
        self.count = 0
    def build(self):
        return
    def button_add_pressed(self):
        self.count += 1
        the_label = self.root.ids.label
        the_label.text = f"Count {self.count}"
    def button_sub_pressed(self):
        self.count -= 1
        the_label = self.root.ids.label
        the_label.text = f"Count {self.count}"

test = quiz39()
test.run()
```
```kv
from kivymd.app import MDApp
class quiz39(MDApp):
    def __init__(self, **kwargs):
        super().__init__(**kwargs)
        self.count = 0
    def build(self):
        return
    def button_add_pressed(self):
        self.count += 1
        the_label = self.root.ids.label
        the_label.text = f"Count {self.count}"
    def button_sub_pressed(self):
        self.count -= 1
        the_label = self.root.ids.label
        the_label.text = f"Count {self.count}"

test = quiz39()
test.run()
````


https://github.com/NaomiRozenberg/unit-3-/assets/142605919/b6c12ec3-9963-40e7-bb6f-658bdac28f80

