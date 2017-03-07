# Автозапуск тестов

Скрипт перед попыткой отправить коммит запускает тесты из ```tests.py``` в случае провала - коммит отправлен не будет и в консоль выведется сообщение

# Как использовать

файл ```pre-commit``` скопировать в папку .git/hooks

# Пример использования

```#!bash

(env) E:\Users\14_pre_commit_hook>git commit -m "initial commit"
.E..
======================================================================
ERROR: test_returns_none_for_complex_solution (tests.QuadraticEquationTestCase)
----------------------------------------------------------------------
Traceback (most recent call last):
  File "E:\Users\14_pre_commit_hook\tests.py", line 22, in test_returns_none_for_complex_solution
    root1, root2 = get_roots(1, 2, 3)
  File "E:\Users\14_pre_commit_hook\quadratic_equation.py", line 6, in get_roots
    root1 = (-b - sqrt(discriminant)) / (2 * a)
ValueError: math domain error

----------------------------------------------------------------------
Ran 4 tests in 0.001s

FAILED (errors=1)
> Tests DID NOT pass

```

# Project Goals

The code is written for educational purposes. Training course for web-developers - [DEVMAN.org](https://devman.org)
