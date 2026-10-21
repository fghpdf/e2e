---
"e2e": patch
---

`app.screenshot()` returns the absolute path of the file it wrote. It returned a path relative to the attempt directory, which resolved to a file that did not exist.
