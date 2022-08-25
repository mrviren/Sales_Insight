## Sales Insights Data Analysis Project


Link to Dashboard - https://prod-apnortheast-a.online.tableau.com/t/salesinsightdashboard/views/ProfitAnalysis/DashboardProfitanalysis?:origin=card_share_link&:embed=n

1. SQL database dump is in db_dump.sql file above. Download `db_dump.sql` file to your local computer and import it.
### Data Analysis Using SQL

1. Show all customer records

    `SELECT * FROM customers;`

1. Show total number of customers

    `SELECT count(*) FROM customers;`

1. Show transactions for Chennai market (market code for chennai is Mark001

    `SELECT * FROM transactions where market_code='Mark001';`

1. Show distrinct product codes that were sold in chennai

    `SELECT distinct product_code FROM transactions where market_code='Mark001';`

1. Show transactions where currency is US dollars

    `SELECT * from transactions where currency="USD"`

1. Show transactions in 2020 join by date table

    `SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;`

1. Show total revenue in year 2020,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";`
	
1. Show total revenue in year 2020, January Month,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");`

1. Show total revenue in year 2020 in Chennai

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020
and transactions.market_code="Mark001";`


<img width="554" alt="image" src="https://user-images.githubusercontent.com/66819985/186597337-32415497-3351-4664-b9d3-75210ad5776c.png">
<img width="554" alt="image" src="https://user-images.githubusercontent.com/66819985/186597470-fc86d50b-8ebe-416f-8346-b93c9ceee8f0.png">



