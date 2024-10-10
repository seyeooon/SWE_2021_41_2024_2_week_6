# SWE_2021_41_2024_2_week_6
---
## Week 4 Assignment
 * https://github.com/seyeooon/SWE_2021_41_2024_2_week_4

```python
def summ(n) :
    x = 0
    while n // 1 != 0 :
        x += (n % 10) ** 2
        n = int(n / 10)
    return (x)


def isHappy(n) :
  while 1 :
      n = summ(n)
      if n == 1 :
          return True
          break
      elif n == 4 :
          return False
          break

isHappy(2)
```
 * Descripttion of your code

---
## Week 5 Assignment
>```docker
>docker exec ossp-container cat /etc/os-release
>```
> * Explanation of your commandline and your output
