``` py
from kivymd.app import MDApp

class quiz40(MDApp):
    def build(self):
        return

    def button_pressed(self):
        button_color = self.root.ids.text
        button_color.md_bg_color = "black"
        button_color.color = "white"

test = quiz40()
test.run()
```

```py
Screen:
    size: 500,500

    MDLabel:
        id: text
        text: "Naomi"
        pos_hint: {"x_center":.5, "y_center":.5}
        font_size: "45pt"
        halign: "center"

    MDRaisedButton:
        id: button
        size_hint: .1, .1
        font_size: "10pt"
        text: "Dark mode"
        on_press:
            app.button_pressed()
```


Uploading Screen Recording 2024-02-03 at 19.59.28.mov…

