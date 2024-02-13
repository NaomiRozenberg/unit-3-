
Create the UML Diagram


<img width="459" alt="Screenshot 2024-02-07 at 11 03 34" src="https://github.com/NaomiRozenberg/unit-3-/assets/142605919/d6e9ee81-e1f6-4b40-9ff4-e64b8eb6709c">



Create the SQL queries to find the responsible for the fraudulent transaction.
SELECT
    d.account_id,
    COALESCE(d.deposit_amount, 0) - COALESCE(w.withdraw_amount, 0) AS net_amount,
    a.balance,
    a.account_type,
    t.date
FROM
    (SELECT
         account_id, SUM(amount) AS deposit_amount
     FROM
         transactions
     WHERE
         transaction_type = 'deposit'
     GROUP BY
         account_id) AS d
LEFT JOIN

    (SELECT
         account_id, SUM(amount) AS withdraw_amount
     FROM
         transactions
     WHERE
         transaction_type = 'withdraw'
     GROUP BY
         account_id) AS w ON d.account_id = w.account_id
LEFT JOIN
    accounts AS a ON d.account_id = a.account_id
LEFT JOIN

    transactions AS t ON d.account_id = t.account_id
WHERE
    COALESCE(d.deposit_amount, 0) - COALESCE(w.withdraw_amount, 0) != a.balance and  a.balance > net_amount;


    <img width="1470" alt="Screenshot 2024-02-13 at 15 32 31" src="https://github.com/NaomiRozenberg/unit-3-/assets/142605919/92ee75ed-fafc-4af7-9a7c-7962ecb0382b">

What is the name of the customer and the problem that resulted in the bankruptcy of the bank?
<img width="1470" alt="Screenshot 2024-02-13 at 15 33 30" src="https://github.com/NaomiRozenberg/unit-3-/assets/142605919/c824c6a4-a341-4b31-ad8e-2108d9b0a30b">
