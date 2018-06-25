oracle 某一列的记录相同的数量大于1的条数
```sql
select t1.arehousing_stock_pk from mm_resource_predistribution t1
 group by t1.warehousing_stock_pk having count(*) > 1
```

同时更新两张表
```sql
update table_name_0 as t1, table_name_1 as t2 set 
t1.value = dummy_value_0,
t2.value = dummy_value_1
where t1.productId = t2.productId
and t1.dateCreated < '2004-01-01'
```
