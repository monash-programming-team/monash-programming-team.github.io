---
layout: page
tag: wiki
---

## Common reasons for "Wrong Answer"

### Extra output

{% highlight python %}
a = input("type an integer:")
{% endhighlight %}
  will produce extra output `type an integer:`, and online judge will regard this as a part of your answer and
gives you `WA` verdict.

### Floating-point error

When you use `==` operator to check the equivalence, floating-point error may give you wrong result, 
for example `1.0/3.0 * 3 == 1` may be `False`; you should always use `abs` (or `fabs` in python) to compare float values.

Also notice that floating-point error can be accumulated,  for example:
```python
# count (1 + ... + n) * m
for i in range(m):
  total += n * (n+1) / 2.0

total == n * (n+1) / 2.0 * m
```
Might be `False`.

Thus, be careful on `float` types:

* whenever you can use integers, do not use float
* in python, whenever you can use `//` (integer division), do not use `/` (float division).
