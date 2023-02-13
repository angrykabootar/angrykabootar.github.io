## Collection of Redis command comes related to data modification.

---

#### Delete all keys from redis matching a pattern

```
redis-cli KEYS "prefix:*" | xargs redis-cli DEL
```
