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
