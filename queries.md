# Database Queries

## Find all customers with postal code 1010
SELECT * FROM customers where postalcode = 1010;
## Find the phone number for the supplier with the id 11
SELECT phone from suppliers where supplierId = 11;
## List first 10 orders ever places, descending by the order date
SELECT * from orders order by orderdate desc limit 10;
## Find all customers that live in London, Madrid, or Brazil
SELECT * from Customers where city = 'London' or city = 'Madrid' or country = 'Brazil';
## Add a customer record for "The Shire", the contact name is "Bilbo Baggins" the address is -"1 Hobbit-Hole" in "Bag End", postal code "111" and the country is "Middle Earth"
Insert into customers (Country, CustomerName, ContactName, Address, City, PostalCode) Values ('Middle Earth', 'The Shiro', 'Bilbo Baggins', '1 Hobbit-Hole', 'Bag End', '111');
## Update Bilbo Baggins record so that the postal code changes to "11122"
Update Customers Set PostalCode = '11122' where CustomerName = 'The Shire';
## (Stretch) Find a query to discover how many different cities are stored in the Customers table. Repeats should not be double counted

## (Stretch) Find all suppliers who have names longer than 20 characters. You can use `length(SupplierName)` to get the length of the name
