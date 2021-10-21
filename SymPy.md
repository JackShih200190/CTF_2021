 ## [SymPy](https://zh.wikipedia.org/wiki/SymPy)
 - SymPy是一個符號計算的Python庫。
 - 它的目標是成為一個全功能的計算機代數系統，同時保持代碼簡潔、易於理解和擴展。
 - 它完全由Python寫成，不依賴於外部庫。
 - SymPy支持符號計算、高精度計算、模式匹配、繪圖、解方程、微積分、組合數學、離散數學、幾何學、概率與統計、物理學等方面的功能。


## SymPy wiki範例
![image](https://user-images.githubusercontent.com/55253641/138242282-6f223b26-265d-416c-8d08-a5954355cf90.png)

## 環境建置
```
!pip install sympy
```

## 解簡單方程式
```python
from sympy import *
x = Symbol('x')
y = Symbol('y')
print(solve([2 * x - y - 3, 3 * x + y - 7],[x, y]))
```
## 資料來源
 - [解方程式](https://www.itread01.com/p/439806.html)
 - 
