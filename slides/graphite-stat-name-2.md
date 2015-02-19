## Stats - What's in a Name?

Many [query functions](http://graphite.readthedocs.org/en/latest/functions.html) allow wildcards like this:

```
averageSeries(my.company.server.*.requests.500)
```

With the wildcard syntax, graphite will look in all subdirectories of `my/company/server` for any stat in a subdirectory at `requests/500`. Graphite will combine all the values and, for this function, anyway, average them.
