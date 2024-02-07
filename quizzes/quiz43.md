1. How many tables are there in the database?
   4
   
2. How many Male inhabitants are Friendly?
     select count(*)from INHABITANT where gender = 'Male' and state ='Friendly'/ 4
   
3. What is the average gold by village?
   select villageid, avg(gold) from INHABITANT group by villageid / 1 = 129.16666666666666, 2 = 112.5 3= 137.5, 4 = 118.75
       
4. How many items are there that start with the letter “A”
     select count(*) from ITEM where item LIKE 'A%' / 3
   
5. How many different jobs are there?
      select distinct count(job) from INHABITANT / 20 

6. What are the items owned by the herbalists?
      select personid from INHABITANT where job='Herbalist' / 4,18
      select item from ITEM where owner=4 or owner=18 / Dagger


      
