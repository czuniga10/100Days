Day 40 | 2 hours
Total: 66 hours

Udacity FSND

Big Networks 

traceroute google.com - lists the different routers that your packets touch on the way to their destination

When routers are misconfigured, they can cause infinite loops. A solve for this is to have a TimeToLive clock on each packet, and once it's reached its max time, it kills itself and sends an error message back to the host letting it know where it died. How traceroute works, is to basically have a packet go to each router on its way to its destination, but kill itself each step of the way in order to get an error message back with the address of the router it was killed at. 

Data & Tables - concepts

Relational databases are stored in tables

All values have in a column have to be the same type

Table Header = Name of table and columns
Table Body = Data within table

Aggregations - DB operation that summarizes multiple rows into a single row. ie (count, ave, max, min, sum)

When writing queries, using the "as" keyword, you can rename the column name

Primary Key - provide uniqueness to your data

