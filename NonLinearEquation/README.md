# 非线性方程求根

>求方程<a href="https://www.codecogs.com/eqnedit.php?latex=f(x)&space;=&space;x^3&space;&plus;&space;x^2&space;-3x&space;-&space;3" target="_blank"><img src="https://latex.codecogs.com/png.latex?f(x)&space;=&space;x^3&space;&plus;&space;x^2&space;-3x&space;-&space;3" title="f(x) = x^3 + x^2 -3x - 3" /></a>在 1.5 附近的根。(误差限<a href="https://www.codecogs.com/eqnedit.php?latex=\varepsilon&space;=&space;1e-6" target="_blank"><img src="https://latex.codecogs.com/png.latex?\varepsilon&space;=&space;1e-6" title="\varepsilon = 1e-6" /></a>，<a href="https://www.codecogs.com/eqnedit.php?latex=\eta&space;=&space;1e-9" target="_blank"><img src="https://latex.codecogs.com/png.latex?\eta&space;=&space;1e-9" title="\eta = 1e-9" /></a>)
>
>1. 编程实现二分法，并求解上述非线性方程的根(有根区间自己确定)。
>2. 编程实现 Newton 法的计算程序，并且选择**不同**的初值(给出至少5个)，观察初值对算法收敛性的影响，当算法收敛时，记录所需的迭代次数和迭代结果，并进行比较。
>3. 分别设计单点弦截法和两点弦截法，计算原方程的根，在初值和容许误差相同的条件下比较它们的收敛速度。

## 思考

1. 比较二分法和牛顿法在非线性方程求根中的优缺点和收敛速度。

	参考：二分法简单易行，但只有线性收敛速度；

	Newton 法计算简单，对于单根情形具有二阶局部收敛速度，但对初值的选择比较困难，Newton 法每次迭代要计算<a href="https://www.codecogs.com/eqnedit.php?latex=f'(x)" target="_blank"><img src="https://latex.codecogs.com/png.latex?f'(x)" title="f'(x)" /></a>，增加了计算量，对于重根情形仅线性收敛。

2. 改进 Newton 迭代法，使其对于重根也具有较高的收敛阶，试写出你所能想到的改进思路及其迭代格式，并简单分析收敛速度。

 ## 说明

1. 文件目录下的`dichotomy.py`, `newton_iteration.py`, `one_point_chord.py` 和 `secant_method.py` 分别对应题目的**二分法**，**Newton 法**，**单点弦截法**和**两点弦截法**。
2. 该方程有三个根，分别是<a href="https://www.codecogs.com/eqnedit.php?latex=x_1&space;=&space;-\sqrt{3},&space;x_2&space;=&space;-1,&space;x_3&space;=&space;\sqrt{3}" target="_blank"><img src="https://latex.codecogs.com/png.latex?x_1&space;=&space;-\sqrt{3},&space;x_2&space;=&space;-1,&space;x_3&space;=&space;\sqrt{3}" title="x_1 = -\sqrt{3}, x_2 = -1, x_3 = \sqrt{3}" /></a>，本题是求解<a href="https://www.codecogs.com/eqnedit.php?latex=\sqrt{3}" target="_blank"><img src="https://latex.codecogs.com/png.latex?\sqrt{3}" title="\sqrt{3}" /></a>的值。