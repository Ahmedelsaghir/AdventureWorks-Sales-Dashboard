# AdventureWorks-Sales-Dashboard
![Adve](https://github.com/Ahmedelsaghir/AdventureWorks-Sales-Dashboard/assets/69742253/256ce3e9-b3a0-4feb-afec-1f4cf84164f5)


![adven](https://github.com/Ahmedelsaghir/AdventureWorks-Sales-Dashboard/assets/69742253/b465e7c2-0256-4d34-aae3-1419c1337962)


AdventureWorks
- Data Source: OLTP
https://docs.microsoft.com/en-us/sql/samples/adventureworks-install-configure?view=sql-server-ver15&tabs=ssms

Conductivity Mode => DirectQuery

Tables:
Sales.SalesOrderHeader
Sales.SalesOrderDetail
Sales.vSalesPerson (view)
Sales.SalesTerritory
Purchasing.ShipMethod
Production.Product
Production.ProductSubcategory
Production.ProductCategory

Create Status (Add based on ufnGetSalesOrderStatusText function)
Create Dates table 

-Rename Tables, columns
-Remove unused columns 

-Denormalized into one table (Merge M Language)
Production.Product
Production.ProductSubcategory
Production.ProductCategory

Contains: PorductID, Product, SubCategory, Category

Solve TotalDue, Tax and Fright by Power Query or DAX 

Modelig:

- Star Schema 
- Product Hierarchy


- line chart vs. counts (USERELATIONSHIP)
orderdate
shipdate
duedate

Model => Star Schema

Measures
- Total no. of Orders Measure 
- Total SubTotal Measure 
- Total Tax Measure 
- Total Freight Measure 
- Total Due Measure 
- Total no. of Qty
- Total no. of Products
  
create DAX table that contains all measures

Visuals: (Use Measures)

- Drill Down
- Drill Through 
- Tooltip page

- Total no. of Orders Card
- Total SubTotal Card
- Total Tax Card
- Total Freight Card
- Total Due Card

- Total no. of Orders by OrderDate vs. ShipDate vs. DueDate
- Total no. ofOrders by Status
- Total no. of Orders by Shipmethod
- Total no. of Orders by Category, SubCategory, Product
- Total no. of Orders by FlagOnlineOffline
- Total no. of Orders vs. TotalDue by Territory
- Top 10 Sales Perosns (# Orders or Total Amount)
- Products by category
- Subtotal by year
- Subtotal by sales person
- Total due vs orders by territory
- Top 10 products by subtotal
