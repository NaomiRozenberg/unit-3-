```py
from kivymd.app import MDApp
from kivy.core.window import Window
from kivymd.uix.button import MDFlatButton

class MyButton(MDFlatButton):
    pass
class TicTacToe(MDApp):
    def build(self):
        Window.size = (500, 500)
        pass
    def button_pressed(self, btn):
        btn.md_bg_color = "yellow"
        if self.root.ids.player_turn.text == "X player's turn":
            btn.text = "X"
            self.root.ids.player_turn.text = "Y player's turn"
        else:
            self.root.ids.player_turn.text = "X player's turn"
            btn.text = "O"
            btn.md_bg_color = "blue"


test = TicTacToe()
test.run()
```

```py
Screen:
    size: 500, 500
    MDBoxLayout:
        size_hint: 1, 1
        md_bg_color:"black"
        orientation: "vertical"

        MDBoxLayout:
            orientation: "horizontal"
            size_hint: 1, 0.25
            md_bg_color:"white"


            MDLabel:
                id: player_turn
                text: "X player's turn"
                font_size: "30pt"
                halign: "left"

        MDBoxLayout:
            orientation: "horizontal"
            size_hint: 1, 0.25
            md_bg_color:"yellow"
            MyButton:
            MyButton:
            MyButton:

        MDBoxLayout:
            orientation: "horizontal"
            size_hint: 1, 0.25
            md_bg_color:"white"
            MyButton:
            MyButton:
            MyButton:

        MDBoxLayout:
            orientation: "horizontal"
            size_hint: 1, 0.25
            md_bg_color:"yellow"
            MyButton:
            MyButton:
            MyButton:

<MyButton>:
    size_hint: 1, 1
    color: "white"
    md_bg_color:"black"
    font_size: "35pt"
    on_press:
        app.button_pressed(self)
```


Uploading Screen Recording 2024-02-03 at 21.31.19.mov…

