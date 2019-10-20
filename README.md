SELECT FirstName, LastName, Title, TitleOfCourtesy, BirthDate FROM employees order by 2; ---- Çalışanın adı, soyadı, ünvanı, görevi, işe başlama tarihi
select CategoryID, CategoryName, FirstName, Phone from categories ----- Müşterinin firma adını, temsilcisini ve telefonunu


Select Quantity, UntilPrice from [Order Details] order by 2; ---- Siparişin adetini ve satış fiyatını

Select CategoryID, CategoryName from Categories order by 2;  ---- Kategori adını

select CategoryID, ProductName, FirstName, LastName, CustomerID, Quantity, QuantityPerUnit from [Order Details] as OD join Products as P on OD.ProductID=P.ProductID join Orders as O on OD.OrderID=O.OrderID Join Employees as E on E.EmployeeID=O.EmployeeID ORDER BY 2;  ---- Bir siparişin hangi çalışan tarafından hangi müşteriye hangi kategorideki üründen hangi fiyattan kaç adet satıldığını listeleyiniz.
