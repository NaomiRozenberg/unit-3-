```py
from my_lib import check_password
from my_lib import DatabaseBridge

x = DatabaseBridge('bitcoin_exchange.db')
transactions = x.search('select * from ledger', multiple=True)
for row in transactions:
    id = row[0]
    sender_id = row[1]
    receiver_id = row[2]
    amount = row[3]
    hash = row[4]
    text = (f"id {id},sender_id {sender_id},receiver_id {receiver_id},amount {amount}")
    if check_password(hash, text):
        print(f"Tx(id={id})Signature matches")
    else:
        print(f"Tx(id={id})Error signature")
```
<img width="1470" alt="Screenshot 2024-02-19 at 10 28 28" src="https://github.com/NaomiRozenberg/unit-3-/assets/142605919/2156ff55-c7db-4d2a-a3e6-b806d568f346">


![IMG_31F3E4057828-1](https://github.com/NaomiRozenberg/unit-3-/assets/142605919/d9e9cb4c-51f6-4031-8236-5adcbf90f3be)
