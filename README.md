SELECT FirstName, LastName, Title, TitleOfCourtesy, BirthDate FROM employees order by 2; ---- Çalışanın adı, soyadı, ünvanı, görevi, işe başlama tarihi
select CategoryID, CategoryName, FirstName, Phone from categories ----- Müşterinin firma adını, temsilcisini ve telefonunu


Select Quantity, UntilPrice from [Order Details] order by 2; ---- Siparişin adetini ve satış fiyatını

Select CategoryID, CategoryName from Categories order by 2;  ---- Kategori adını

SELECT        dbo.Employees.LastName, dbo.Employees.FirstName, dbo.Employees.TitleOfCourtesy, dbo.Employees.Title, dbo.Employees.HireDate, dbo.Products.UnitsInStock, dbo.Products.UnitPrice, dbo.Products.ProductName, 
                         dbo.[Order Details].Quantity, dbo.Categories.CategoryName, dbo.Customers.ContactName, dbo.Customers.ContactTitle, dbo.Customers.CompanyName, dbo.Customers.Phone, dbo.[Order Details].UnitPrice AS Expr1
FROM            dbo.Orders INNER JOIN
                         dbo.Employees ON dbo.Orders.EmployeeID = dbo.Employees.EmployeeID INNER JOIN
                         dbo.[Order Details] ON dbo.Orders.OrderID = dbo.[Order Details].OrderID INNER JOIN
                         dbo.Products ON dbo.[Order Details].ProductID = dbo.Products.ProductID INNER JOIN
                         dbo.Categories ON dbo.Products.CategoryID = dbo.Categories.CategoryID INNER JOIN
                         dbo.Customers ON dbo.Orders.CustomerID = dbo.Customers.CustomerID  ---- Bir siparişin hangi çalışan tarafından hangi müşteriye hangi kategorideki üründen hangi fiyattan kaç adet satıldığını listeleyiniz.
