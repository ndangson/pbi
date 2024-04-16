**1. Introduction**

Hi there, this is my mini Power BI about sales dashboard of B2B sales dataset.
Objective:
- Creating a self-study Power BI dashboard.
- Testing new features and DAX of Power BI updates monthly.

**2. Dataset overview**

>https://data.world/dataman-udit/us-regional-sales-data
- This dataset has sales data of B2B customers in US across different sales channels: **In-Store, Online, Distributor, and Wholesale**.
- Time: from May-2018 to Dec-2020
- Dimensions (Master data): Customer, Product, SalesTeam, Store
- Fact (Transaction data): Sales
  >Ref: https://www.linkedin.com/pulse/us-regional-sales-project-youki-chiba
  + OrderNumber: A unique identifier for each order.
  + Sales Channel: The channel through which the sale was made (In-Store, Online, Distributor, Wholesale).
  + WarehouseCode: Code representing the warehouse involved in the order.
  + ProcuredDate: Date when the products were procured.
  + OrderDate: Date when the order was placed.
  + ShipDate: Date when the order was shipped.
  + DeliveryDate: Date when the order was delivered.
  + SalesTeamID: Identifier for the sales team involved.
  + CustomerID: Identifier for the customer.
  + StoreID: Identifier for the store.
  + ProductID: Identifier for the product.
  + Order Quantity: Quantity of products ordered.
  + Discount Applied: Applied discount for the order.
  + Unit Cost: Cost of a single unit of the product.
  + Unit Price: Price at which the product was sold.
