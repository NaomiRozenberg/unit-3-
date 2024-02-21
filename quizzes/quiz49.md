```py
from my_lib import DatabaseBridge

x = DatabaseBridge('bitcoin_exchange.db')

create_table = """CREATE TABLE if not exists users(
id INTEGER PRIMARY KEY,
user_id INTEGER NOT NULL, 
name  Text,
email text
)"""

x.run_query(create_table)

add = """INSERT into users (user_id, name, email) values(560,'bob1','bob1@123'),(371,'bob2','bob2@123'),(488,'bob3','bob3@123'),(561,'bob4','bob4@123'),(254,'bob5','bob5@123'),(920,'bob6','bob6@123'),(438,'bob7','bob7@123'),(744,'bob8','bob8@123'),(261,'bob9','bob9@123')
"""
x.run_query(add)

query_1 = "Select * from ledger where receiver_id=920 or sender_id = 920"
result1 = x.search(query=query_1, multiple = True)
print(result1)
x.close()
```
<img width="1470" alt="Screenshot 2024-02-21 at 16 39 15" src="https://github.com/NaomiRozenberg/unit-3-/assets/142605919/963a9213-6c37-425a-be15-bbe8f8fb6d7a">

![JPEG image-4F0C-9A70-CA-0](https://github.com/NaomiRozenberg/unit-3-/assets/142605919/020ffc10-8596-488f-bd16-4c8b7a0b3377)


