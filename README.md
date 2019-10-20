SELECT FirstName, LastName, BirthDate FROM employees order by 2; ---- Çalışanın adı, soyadı, ünvanı, görevi, işe başlama tarihi
select CategoryID, CategoryName, FirstName, Phone from categories ----- Müşterinin firma adını, temsilcisini ve telefonunu


Select Quantity, UntilPrice from [Order Details] order by 2; ---- Siparişin adetini ve satış fiyatını

Select CategoryID, CategoryName from Categories order by 2;  ---- Kategori adını

select E.EmployeeID, FirstName, P.CategoryID, ProductName, C.CategoryID, CategoryName, Quantity, UntilPrice from Employees as E join Categories as C on E.EmployeeID=C.EmployeeID Join Order as O on O.OrderID=E.OrderID join Producs as P on P.CategoryID=C.CategoryID ORDER BY 2;  ---- Bir siparişin hangi çalışan tarafından hangi müşteriye hangi kategorideki üründen hangi fiyattan kaç adet satıldığını listeleyiniz.
