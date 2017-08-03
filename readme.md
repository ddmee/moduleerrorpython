# Problem

Using Python 3.6, cannot run file1.py from the root directory, because of a Module error:

```bash
python lib/shared/file1.py
Traceback (most recent call last):
  File "lib/shared/file1.py", line 1, in <module>
    import lib.shared.file2 as file2
ModuleNotFoundError: No module named 'lib.shared'
```

But, starting the interpreter and importing the module does not cause this problem:

```bash
python
Python 3.6.0 (v3.6.0:41df79263a11, Dec 23 2016, 08:06:12) [MSC v.1900 64 bit (AMD64)] on win32
Type "help", "copyright", "credits" or "license" for more information.
import lib.shared.file1
['Hello', 'Server', '__builtins__', '__cached__', '__doc__', '__file__', '__loader__', '__name__', '__package__', '__spec__']
quit()
```

# Solution
Run the file as a module like:
```bash
python -m lib.shared.file1
```

[From Stackoverflow](https://stackoverflow.com/questions/14132789/relative-imports-for-the-billionth-time)
