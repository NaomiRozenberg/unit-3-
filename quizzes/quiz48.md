```py
from my_lib import check_password
from my_lib import DatabaseBridge

x = DatabaseBridge('bitcoin_exchange.db')
transactions = x.search('select * from ledger', multiple=True)
total_amount = 0
for row in transactions:
    id = row[0]
    sender_id = row[1]
    receiver_id = row[2]
    amount = row[3]
    hash = row[4]
    text = (f"id {id},sender_id {sender_id},receiver_id {receiver_id},amount {amount}")
    if check_password(hash, text):
        total_amount += amount
print(total_amount)
```
<img width="1470" alt="Screenshot 2024-02-19 at 10 21 57" src="https://github.com/NaomiRozenberg/unit-3-/assets/142605919/65510261-158c-43b0-8b98-e0899cf15080">


![IMG_70F2B2C9C05D-1](https://github.com/NaomiRozenberg/unit-3-/assets/142605919/08e7ca69-0eed-483a-bada-2f83e8c8b735)
