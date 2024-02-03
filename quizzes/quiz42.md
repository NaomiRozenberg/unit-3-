```py
from kivymd.app import MDApp
from kivymd.uix.screen import MDScreen

class Mystery_page_A(MDScreen):
    pass

class Mystery_page_B(MDScreen):
    pass
class Mystery(MDApp):
    def build(self):
        return

test = Mystery()
test.run()
```

```py
ScreenManager
    Mystery_page_A:
        name: "Mystery_page_A"
    Mystery_page_B:
        name: "Mystery_page_B"

<Mystery_page_A>:
    MDLabel:
        id: text
        text: "Mystery_page_A"
        pos_hint: {"x_center":.5, "y_center":.5}
        font_size: "45pt"
        halign: "center"
    MDRaisedButton:
        text:"Go to Mystery Page B"
        on_press:
            root.parent.current = "Mystery_page_B"

<Mystery_page_B>:
    MDLabel:
        id: text
        text: "Mystery_page_B"
        pos_hint: {"x_center":.5, "y_center":.5}
        font_size: "45pt"
        halign: "center"
    MDRaisedButton:
        text:"Go to Mystery Page A"
        on_press:
            root.parent.current ="Mystery_page_A"
```


Uploading Screen Recording 2024-02-03 at 20.15.36.mov…

<img width="563" alt="Screenshot 2024-02-03 at 22 01 16" src="https://github.com/NaomiRozenberg/unit-3-/assets/142605919/643b9862-198a-4385-9734-fb3bc67faf77">
