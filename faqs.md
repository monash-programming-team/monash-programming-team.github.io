---
layout: page
---

# FAQs

> **Q:** Why I passed all samples, but still get `Wrong Answer (WA)` ?

* There are multiple secret test cases; in classic rules, failing on any of them causes `Wrong Answer`, so you will have to spot the bug by yourself.

* Another common reason cauase `WA` even your algorithm is fully correct is **extra output** , for example 
```python
a = input("type an integer:")
```
will produce extra output `type an integer:`, and online judge will regard this as a part of your answer and gives you `WA` verdict.

---

> **Q:** What is `Time Limit Exceeded (TLE)` ?

* Your program runs out of time limit; this error doesn't allow you to
  know if your program would reach the correct solution to the problem
  or not.

---

> **Q:** What is `Memory Limit Exceeded (MLE)`

* Your program tried to use more memory than the judge allows. 

---

> **Q:** What is `Runtime Error (RE)`

* Your program failed during the execution (segmentation fault, floating
  point exception...). The exact cause is not reported to the user to
  avoid hacking. 

---

> **Q:** There are `Input file: standard input`, `Output file: standard output` 
in my problem statement, what do these mean? Do I need to create files?

* Reading from standard input (`stdin`) means reading data which
you are typing on your keyboard, and outputting to standard output
(`stdout`) means printing data to your console. So it's not
necessary to create files.
