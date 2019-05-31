# How can I recover a file I wrongly removed?

```shell
git rm <filename> # Ouch!
# Then just run following two liens.
git reset HEAD ./<filename>
git checkout ./<filename>
```
