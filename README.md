# happy_birthday_py_exe
An easy happy birthday program by python, and distribute in exe. 

## 1.Results:
![image](https://github.com/Thinkin99/happy_birthday_py_exe/blob/main/result.png)



## 2.Code：

```python
import tkinter as tk
import random
import threading
import time
def windows():
    window = tk.Tk()
    width=window.winfo_screenwidth()
    height=window.winfo_screenheight()
    a=random.randrange(0,width)
    b=random.randrange(0,height)
    window.title('生日快乐')
    window.geometry("300x70"+"+"+str(a)+"+"+str(b))
    tk.Label(window,        text='生日快乐！',    # 标签的文字
             bg='white',     # 背景颜色
             font=('黑体', 20),     # 字体和字体大小
             width=30, height=3  # 标签长宽
             ).pack()    # 固定窗口位置
    window.mainloop()
threads = []
for i in range(200):#需要的弹框数量
    t = threading.Thread(target=windows)
    threads.append(t)
    time.sleep(0.01)
    threads[i].start()
```

## 3.py—>exe

`pip install pyinstaller`

`pyinstaller -F -W %{PATH OF YOUR FILE}`

## 4.send to your friends!
