
Results of SSIS
===============

# Files Reviewed


This is the following items which are analyzed

LoadXMLData.dtsx
DataTransfer.dtsx
# LoadXMLData.dtsx


-- {www.microsoft.com/sqlserver/dts/tasks/sqltask}SqlTaskData
IF NOT EXISTS (SELECT * FROM AdventureWorks.sys.tables WHERE type ='U' and name = 'OrderDatesByCountryRegion')
CREATE TABLE [OrderDatesByCountryRegion]
(
    [ShipCountryRegion] NVARCHAR(50),
    [ShipCountryRegionCount] INT,
    [OldestOrderDate] DATETIME,
    [NewestOrderDate] DATETIME
)
ELSE
TRUNCATE TABLE OrderDatesByCountryRegion

# Paths


This is pths listed

id
373
name
orders
description

startId
19
endId
367
id
1169
name
HasCountryRegion
description

startId
396
endId
1160
id
1277
name
Aggregate Output 1
description

startId
1161
endId
1273
# DataTransfer.dtsx


-- {www.microsoft.com/sqlserver/dts/tasks/sqltask}SqlTaskData
IF NOT EXISTS (SELECT * FROM AdventureWorks.sys.tables WHERE type ='U' and name = 'HighIncomeCustomers')
CREATE TABLE dbo.HighIncomeCustomers 
(
[FirstName] nvarchar(50),
[MiddleInitial] nchar(1),
[LastName] nvarchar(50),
[BirthDate] datetime,
[MaritalStatus] nchar(1),
[Gender] nchar(1),
[EmailAddress] nvarchar(50),
[YearlyIncome] money,
[TotalChildren] tinyint,
[NumberChildrenAtHome] tinyint,
[Education] nvarchar(50),
[Occupation] nvarchar(50),
[HouseOwnerFlag] bit,
[NumberCarsOwned] tinyint,
[AddressLine1] nvarchar(60),
[AddressLine2] nvarchar(60),
[City] nvarchar(30),
[State] nvarchar(3),
[ZIP] nvarchar(10),
[Phone] nvarchar(50)
)
ELSE
TRUNCATE TABLE AdventureWorks.dbo.HighIncomeCustomers 

# Paths


This is pths listed

id
236
name
Flat File Source Output
description

startId
133
endId
141
id
299
name
HighIncome
description

startId
264
endId
87
