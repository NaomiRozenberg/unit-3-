```py
import sqlite3

from kivymd.app import MDApp
from my_lib import DatabaseBridge
from passlib.hash import sha256_crypt

hash_funcation = sha256_crypt.using(rounds = 30000)
def get_hash(text:str):
    return hash_funcation.hash(text)

def check_hash(input_hash, text):
    return hash_funcation.verify(text, input_hash)

class quiz46(MDApp):
    def __init__(self, **kwargs):
        super().__init__(**kwargs)
        self.components = {"base":0, "income_tax":0,"inhabitant":0, "pension":0,"health":0, 'total': 0}
        self.my_db = DatabaseBridge("payments.db")

    def build(self):
        return

    def save(self):
        pass

    def update(self):
        base = self.root.ids.base.text
        if base:
            total = int(base)


            income_tax = total*int(self.root.ids.income_tax.text or '0' ) // 100
            self.root.ids.income_tax_label.text = f"{income_tax} JPY"

            inhabitant = total*int(self.root.ids.inhabitant.text or '0') // 100
            self.root.ids.inhabitant_label.text=f"{inhabitant} JPY"

            pension = total*int(self.root.ids.pension.text or '0') // 100
            self.root.ids.pension_label.text = f"{pension} JPY"

            health = total*int(self.root.ids.health.text or '0') // 100
            self.root.ids.health_label.text = f"{health} JPY"

            total = total - inhabitant - income_tax - pension - health
            hash = f"base{base}, inhabitant{inhabitant}, income_tax{income_tax},pension{pension},health{health},total{total}"

            self.root.ids.salary_label.text = f"{total}JYP"
            self.components['base'] = int(base)
            self.components['inhabitant'] = inhabitant
            self.components['health'] = health
            self.components['pension'] = pension
            self.components['income_tax'] =income_tax
            self.components['total'] = total
            self.components['hash'] = hash
            ids = ["inhabitant", "income_tax", "pension", "health"]

    def save(self):
        hash = self.components['hash']
        base = self.components['base']
        inhabitant = self.components['inhabitant']
        health = self.components['health']
        pension = self.components['pension']
        total = self.components['total']
        income_tax = self.components['income_tax']

        query = f"""INSERT into payments(base, inhabitant, income_tax, pension, health, total,hash) 
        values({base}, {inhabitant}, {income_tax}, {pension}, {health}, {total},'{hash}')
         """
        self.my_db.run_query(query)
        self.root.ids.hash.text = f"Payment saved"


    def clear(self):
        for label in ["base", "inhabitant","income_tax","pension","health"]:
            self.root.ids[label].text = ""
            self.root.ids[label+"_label"].text = " JPY"

        self.root.ids["salary_label"].text = " JPY"
        self.root.ids.hash.text = "----"


test = quiz46()
create = """CREATE TABLE if not exists payments(
    id INTENGER PRIMARY KEY, 
    base int, 
    inhabitant int, 
    income_tax int, 
    pension int, 
    health int, 
    total int, 
    hash Text

    )"""
db = DatabaseBridge("payments.db")
db.run_query(create)
db.close()
test.run()
```
<img width="1470" alt="Screenshot 2024-02-15 at 10 49 41" src="https://github.com/NaomiRozenberg/unit-3-/assets/142605919/78c09f59-3507-4ab2-a3f9-8b3ed6efb75b">
