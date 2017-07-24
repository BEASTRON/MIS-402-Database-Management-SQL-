# MIS-402-Database-Management-SQL-

#//Examples & formats from http://www.w3schools.com/sql/default.asp


CREATE TABLE CUSTOMERS
(
CustomerID int NOT NULL,
CustomerName varchar(255),
CustomerAddress varchar(255),
CustomerCity varchar(255),
CustomerState varchar(255),
CustomerPostalCode varchar(255)
INSERT INTO CUSTOMERS(CustomerID, CustomerName, CustomerAddress, CustomerCity, CustomerState, CustomerPostalCode)
VALUES('1','Contemporary Casuals','1355 Hines Blvd.','Gainsville','FL','32601-2871');
VALUES('2','Value Furniture','15145 S.W. 17th St.','Plano','TX','75094-7743');
VALUES('3','Home Furnishings','1900 Allard Ave.','Albany','NY','12209-1125');
VALUES('4','Eastern Furniture','1925 Beltline Rd.','Carteret','NJ','07008-3188');
VALUES('5','Impressions','5585 Westcott Ct.','Sacramento','CA','94206-4056');
VALUES('6','Furniture Gallery','325 Flatiron Dr.','Boulder','CO','80514-4432');
VALUES('7','Period Furniture','394 Rainbow Dr.','Seattle','WA','97954-5589');
VALUES('8','California Classics','816 Peach Rd.','Santa Clara','CA','96915-7754');
VALUES('9','M and H Casual Furniture','3709 First St.','Clearwater','FL','34620-2314');
VALUES('10','Seminole Interiors','2400 Rocky Point Dr.','Seminole','FL','34646-4423');
VALUES('11','Merican Euro Lifestyles','2424 Missouri Ave. N.','Prospect Park','NJ','07508-5621');
VALUES('12','Battle Creek Furniture','345Capital Ave. SW','Battle Creek','MI','49015-3401');
VALUES('13','Heritage Furnishings','66789 College Ave.','Carlisle','PA','17013-8834');
VALUES('14','Kaneohe Homes','112 Kiowai St.','Kaneohe','HI','96744-2537');
VALUES('15','Mountain Scenes','4132 Main Street','Ogden','UT','84403-4432');
);



CREATE TABLE ORDERS
(
OrderID int NOT NULL,
OrderDate varchar(255),
OrderDate varchar(255),
PRIMARY KEY(OrderID),
FOREIGN KEY(CustomerID) REFERENCES Customers(CustomerID),
INSERT INTO ORDERS(OrderID, OrderDate, CustomerID)
VALUES('1001','10/21/2010','1');
VALUES('1002','10/21/2010','8');
VALUES('1003','10/22/2010','15');
VALUES('1004','10/22/2010','5');
VALUES('1005','10/24/2010','3');
VALUES('1006','10/24/2010','2');
VALUES('1007','10/27/2010','11');
VALUES('1008','10/30/2010','12');
VALUES('1009','11/5/2010','4');
VALUES('1010','11/5/2010','1');
);


SELECT CustomerName
FROM CUSTOMERS
where CustomerState = CA, WA
ORDER BY CustomerPostalCode DESC


