```py
from my_lib import DatabaseBridge

x = DatabaseBridge('quiz45.db')


haiku = """Code flows like a stream
Algorithms guide its way
In silence, it solves"""

haiku_without_commas = haiku.replace(',', '')


create = """CREATE TABLE if not exists WORDS (
 id INTEGER PRIMARY KEY,
 length int, 
 word text
 )"""
x.run_query(query=create)
total = 0
number_of_words = 0
for word in haiku_without_commas.split():
   length = len(word)
   query = f"""insert into  WORDS(length, word) 
    values({length}, '{word}')"""
   x.insert(insert_query=query)
   total += length
   number_of_words += 1
mean = total/number_of_words
x.close()
print("Your mean is", mean)
```
<img width="1470" alt="Screenshot 2024-02-15 at 13 29 20" src="https://github.com/NaomiRozenberg/unit-3-/assets/142605919/0f119edc-2dbc-4c0d-80af-06b072735783">
