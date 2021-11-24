Return an estimate of number of rows in a table

```
SELECT reltuples AS estimate FROM pg_class WHERE relname = 'table_name';
```
