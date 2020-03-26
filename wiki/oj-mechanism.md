---
layout: page
tag: wiki
---

# Online Judge Mechanism

## Standard IO

Most of OJ (Online Judge) use following set up by default:

* `Input file: standard input (stdin)`: reading data which you are typing on your keyboard.

* `Output file: standard output (stdout)`: printing data to your console

If you are fimilar with command line, the following code explains IO

{% highlight sh %}
./<my-program> < test.in > test.out
{% endhighlight%}

This [tutorial](http://linuxcommand.org/lc3_lts0070.php) can help you to understand these concepts.

## File IO

Sometimes you have to use file IO, e.g. `USACO`, some `Codeforces` problems; 
which means the judge assumes your program will read/output from/to a specified file.

The minimum effort to adjust your code from `standard IO` to `file IO` is as follow (`a+b problem`).

* Python

```python
import sys

sys.stdin = open('file.in', 'r')
sys.stdout = open('file.out', 'w')

# doing IO as normal 
a, b = map(int, input().split())
print (a+b)
```

* C++

```c++
#include <bits/stdc++.h>
using namespace std;

int main() {
  freopen("file.in", "r", stdin);
  freopen("file.out", "w", stdout);
  // doing IO as normal
  cin >> a >> b;
  cout << a + b << endl;
  return 0;
}
```

## Judge

### Text-based comparison

OJ uses `text-based comparison` to judge your output in most of cases; 
which means your output will be compared with correct output by each character, 
thus any mismiatching will cause `Wrong Answer` (also see [Common reasons for WA](/wiki/common-wa)), for example

* expect: `hello`; yours: `hello.`

Some smart judge may discard extra whitespaces or newline characters, 
and gives you `Accepted` or `Presentation Error`.


### Special Judge

When the answer is not unique (e.g. some constructive problems), `special judge` will be applied.
There is another program to read your output and parse to data, then make judgement.
If you didn't follow the format as in the problem statement strictly, you will get `Wrong Answer` because of parsing failed.
