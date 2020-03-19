---
layout: nav
---

## PRACTICES

  We typically run training session once a week. You can [join us](contact) to track upcoming events.

---

## WANT TO GET STARTED?!

  If you want to jump in and try a few problems on your own,
  here are a couple websites that host some problems.
  If you have any questions or problems, 
  please contact me and I will help you out in any way that I can!


### 1. Input/Output

Being familiar with IO is the first step, 
there are some common patterns on dealing with IO.

* [Input/output: py, cpp](https://vjudge.net/contest/361612)

  {::options parse_block_html="true" /} 
  <details><summary markdown="span">Python3</summary>
  ```python
  # read two ints
  a, b = map(int, input().strip().split())

  # read a list of ints
  arr = list(map(int, input().strip().split()))
  ```
  </details>
  {::options parse_block_html="false" /}


* [Input/output: cpp only](https://vjudge.net/contest/361790)

  {::options parse_block_html="true" /} 
  <details><summary markdown="span">cpp</summary>
  ```cpp
  // read two ints
  scanf("%d%d", &a, &b);
  
  // or
  cin >> a >> b

  // read a series of ints
  while (scanf("%d", &a) != EOF) {
    // do some thing
  }

  // or
  while (cin >> a) {
    // do some thing
  }
  ```
  </details>
  {::options parse_block_html="false" /}


### 2. Analyze your program

Pay attention to `Time limit, Memory limit` constraints in your problem
statement when you get `Time Limit Exceeded (TLE)` or `Memory Limit Exceeded (MLE)` verticts.

`C++` can nearly run $10^8$ basic operations (e.g. `+, -`) in 1 second; 
while `Python` can nearly run $10^6$ basic operations in 1 second. 
You can estimate your program running time based on these info and your complexity analysis to avoid `TLE` and `MLE`.

### 3. Try some algorithmic problems

It's time to be involved in some problem-solving skill

* [Looping and binary-searching](https://vjudge.net/contest/361685)

  {::options parse_block_html="true" /} 
  <details><summary markdown="span">Binary search</summary>

  ```python
  # my favorite pattern 
  best = None
  while l <= r:         # search space is [l, r]
    m = (l + r) // 2    # choose middle
    if check(m) :       # is m >=  
                        # invariant: all v in [l, r] >=
      l = m + 1         # shrink search space 
      best = m          # best so far
    else:
      r = m - 1         # shrink search space
  return best
  ```
  </details>
  {::options parse_block_html="false" /}

---

### See more in [FAQs](/pages/faq)
