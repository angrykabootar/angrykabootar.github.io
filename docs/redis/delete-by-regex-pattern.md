## Collection of Redis command comes.

---

#### Find all the files not ending with a newline.

```
redis-cli KEYS "prefix:*" | xargs redis-cli DEL
```
