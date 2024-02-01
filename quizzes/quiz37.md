```py
class CompoundIntererst:
    def __init__(self, principal, rate, num_years):
        self.principal = principal
        self.rate = rate
        self.num_years = num_years

    def calculate (self):
        return self.principal * (1+ self.rate)** self.num_years

class  AccountingProgram(CompoundIntererst):
    def __init__(self, principal, rate, num_years):
        super().__init__(principal, rate, num_years)

    def set_principal(self, principal):
        self.principal = principal

    def set_rate(self,rate):
        self.rate = rate

    def set_num_years(self,num_years):
        self.num_years = num_years

    def calculate_interest(self):
        return self.calculate()


accounting_program = AccountingProgram(principal= 100, rate = 0.1,num_years= 20)

interest = accounting_program.calculate_interest()
print("Compound Interest:", interest)
```
<img width="1253" alt="Screenshot 2024-02-01 at 10 13 13" src="https://github.com/NaomiRozenberg/unit-3-/assets/142605919/8180bacc-8360-43ee-b231-e635ef609f09">
