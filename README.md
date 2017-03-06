# Day1
Assignments
# Post your favourite >=3 Table join statement from Test database

SELECT Customers.CustomerName, Orders.OrderID, Orders.EmployeeID, Customers.Address
FROM Customers
INNER JOIN Orders
ON Customers.CustomerID=Orders.CustomerID
ORDER BY Customers.CustomerName;

#Design	SQL	statement	to	create	two	tables	to	store
    – Mutations
    – Samples

CREATE TABLE mutations
(
  GH INTEGER PRIMARY KEY AUTO_INCREMENT NOT NULL,
  DNA  INTEGER NOT NULL,
  reference_base   VARCHAR(1) NOT NULL,
  alternative_base VARCHAR(1) NOT NULL,
  genotypes        VARCHAR(3) NOT NULL,
  chromosome       INTEGER NOT NULL,
  position         INTEGER(78) NOT NULL,
  ATP7A            VARCHAR(3) NOT NULL,
  ATP7B            VARCHAR(3) NOT NULL,
);

CREATE TABLE samples (
  GH            INTEGER PRIMARY KEY AUTO_INCREMENT NOT NULL,
  DNA           INTEGER NOT NULL,
  Staining        VARCHAR(255) NOT NULL,
  QuantitativeCopper VARCHAR(255) NOT NULL,
  AGE               DECIMAL,
  GENDER            BINARY(2),
  );
