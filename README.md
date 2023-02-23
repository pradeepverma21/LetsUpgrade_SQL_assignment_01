# LetsUpgrade_SQL_assignment_01
From the following tables write a query to find the salesperson and customer who
reside in the same city. Return Salesman, custame and city

salesman_id  | name        | city     | commission
_____________+_____________+__________+____________
5001         | James Hoog  | New York |  0.15
5002         | Namil Knite | Paris    |  0.13
5005         | Pit Knite   | London   |  0.11
5006         | Mc Lyon     | Paris    |  0.14
5007         | Paul Adam   | Rome     |  0.13
5003         | Lousen Hen  | San Jose |  0.12



sales_id | cust_name     | city      | grade | salesman_id 
_________+_______________+___________+_______+____________
3002     | Nick Rimando  | New York  | 100   | 5001
3007     | Brad Davis    | New York  | 200   | 5001
3005     | Graham Zusi   | California| 200   | 5002
3008     | Julian Green  | London    | 300   | 5002
3004     | Fabian Johnson| Paris     | 300   | 5006
3009     | Geoff Cameron | Berlin    | 100   | 5003
3003     | Jozy Altidor  | Moscow    | 200   | 5007
3001     | Brad Guzan    | London    |       | 5005

The Query is :

SELECT s.salesman, c.custname, s.city
FROM salesman s
INNER JOIN customer c ON s.city = c.city;
