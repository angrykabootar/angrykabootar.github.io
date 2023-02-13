## Collection of Miscellaneous command comes in handy once in a blue moon.

---

#### Find all the files not ending with a newline.

```
redis-cli KEYS "prefix:*" | xargs redis-cli DEL
```
