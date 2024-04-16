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
  + **OrderNumber**: A unique identifier for each order.
  + **SalesChannel**: The channel through which the sale was made (In-Store, Online, Distributor, Wholesale).
  + **WarehouseCode**: Code representing the warehouse involved in the order.
  + **ProcuredDate**: Date when the products were procured.
  + **OrderDate**: Date when the order was placed.
  + **ShipDate**: Date when the order was shipped.
  + **DeliveryDate**: Date when the order was delivered.
  + **SalesTeamID**: Identifier for the sales team involved.
  + **CustomerID**: Identifier for the customer.
  + **StoreID**: Identifier for the store.
  + **ProductID**: Identifier for the product.
  + **OrderQuantity**: Quantity of products ordered.
  + **DiscountApplied**: Applied discount rate for the order.
  + **UnitCost**: Cost of a single unit of the product.
  + **UnitPrice**: Price at which the product was sold.

**3. Defining measures**
_Sales
- Gross revenue = **[UnitPrice]** * **[OrderQuantity]**
- Cost = **[UnitCost]** * **[OrderQuantity]**
- Discount = Gross Revenue * **[DiscountApplied]**
- Profit = Gross revenue - Cost - Discount
- %Profit = Profit / Gross revenue

_O2D (Order-to-Delivery)
- ProcessingTime (days) = **[ShipDate]** - **[OrderDate]**
- ShippingTime (days) = **[DeliveryDate]** - **[ShipDate]**
- DeliveryTime = ProcessingTime + ShippingTime
