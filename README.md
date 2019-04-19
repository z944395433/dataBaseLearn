### 一些数据库sql收集和整理主要 关于mysql 和postgrep 的一些json操作
##### postgrepSQL

##### jsonb_obeject_agg()

##### 全表获取json中key的数量和其他字段
https://stackoverflow.com/questions/36171737/how-to-count-setof-number-of-keys-of-json-in-postgresql
##### example
select A.id,array_length(array_agg(A.keys), 1) from (
    select id,jsonb_object_keys(info) as keys from s_sys_paper 
) A GROUP BY A.id;


