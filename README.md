# enter
Nicer interface to context variables in practical scenarios.

```pycon
>>> class Foo(ContextClass):
...     x: int | None = None

>>> with Foo.context(x=1):
...     print(Foo.current.x)
```

Works with type hints:

<img width="881" height="182" alt="image" src="https://github.com/user-attachments/assets/abeb517e-36ae-4cf7-8c6f-a1849c6cefde" />
<img width="925" height="216" alt="image" src="https://github.com/user-attachments/assets/a6a2bbe5-00d9-45b6-8603-431c1f6024f0" />
