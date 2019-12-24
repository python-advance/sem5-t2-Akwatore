# sem5-t2
Самостоятельная работа (ИСР, ВСР). 5 семестр, тема 2

[ИСР 2.1, 2.2](https://repl.it/@ulyaakwatore/Siem-5-Tiema-2-ISR-21-22)

Задание 2.1

```
def fib(n):
  fib1=0
  fib2=1
  print(fib1,fib2, end=" ")
  while fib2<n :
    fib_sum = fib1 + fib2
    fib1 = fib2
    fib2 = fib_sum
    if fib2>n: break
    print(fib2, end=" ")

fib(10)
```

Задание 2.2

```
class Fib:
  def __init__(self, k):
    self.k = k

  def __iter__(self):
    self.fib1 = 0
    self.fib2 = 1
    print(self.fib1, self.fib2, end=" ")
    return self

  def __next__(self):
    fib_sum = (self.fib1 + self.fib2)
    self.fib1 = self.fib2
    self.fib2 = fib_sum
    if fib_sum > self.k:
      raise StopIteration
    return fib_sum

for i in Fib(10):
  print (i, end=" ")
```
