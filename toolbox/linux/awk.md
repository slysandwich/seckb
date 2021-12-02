# Awk

## Common Options

* \-F : field separator

```
$ echo "Hello::My::World!" | awk -F "::" '{print $1, $3}'
```
