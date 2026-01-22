# contextclass
Alternative interface to context variables for practical scenarios.

```pycon
>>> from contextclass import ContextLocal, enter, current
>>> from dataclasses import dataclass

>>> @dataclass
... class Foo(ContextLocal):
...     x: int | None = None

>>> @enter(Foo, x=1)
... def f() -> None:
...     print(current(Foo))
>>> f()
Foo(x=1)

>>> with Foo.context(x=2):
...     print(Foo.current.x)
2

>>> @Foo.context(x=3)
... def f() -> None:
...     print(Foo.current.x)
>>> f()
3

```

Works with type hints:

<img width="821" height="454" alt="image" src="https://github.com/user-attachments/assets/6c4f5b4b-48b5-4807-a6aa-bf9cd6b8e3e4" />
