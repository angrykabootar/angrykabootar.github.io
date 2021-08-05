Returns all idle queries for the database in the decreasing order of age.

```
SELECT pid, age(clock_timestamp(), query_start), usename, query 
FROM pg_stat_activity 
WHERE query != '<IDLE>' AND query NOT ILIKE '%pg_stat_activity%' 
ORDER BY age(clock_timestamp(), query_start) desc;
```

Kill running query
```
SELECT pg_cancel_backend(procpid);
```

Kill idle query
```
SELECT pg_terminate_backend(procpid);
```