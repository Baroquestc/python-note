# 04-Octave教程

## 1 基本操作

### 1.1 逻辑运算

```octave
octave:1> 1 == 2
ans = 0
octave:2> 1 ~= 2
ans = 1
octave:3> 1 && 0
ans = 0
octave:4> 1 || 0
ans = 1
octave:5> xor(1,0) %异或
ans = 1
```

### 1.2  其他

#### 1.2.1 更改提示符

```octave
octave:7> PS1('>>')
>>
```

#### 1.2.2 添加分号抑制输出

```octave
octave:7> PS1('>>')
>>a = 1
a =  1
>>a = 1;
>>
```

#### 1.2.3 格式化输出

```octave
>>a = pi
a =  3.1416
>>disp(sprintf('6 decimals: %0.6f',a))
6 decimals: 3.141593
>>disp(sprintf('6 decimals: %0.2f',a))
6 decimals: 3.14
>>format long
>>a
a =  3.141592653589793
>>format short
>>a
a =  3.1416
```

### 1.3 矩阵

- 1-2，每次递增0.1

```octave
>>v = 1:0.1:2
v =
    1.0000    1.1000    1.2000    1.3000    1.4000    1.5000    1.6000    1.7000    1.8000    1.9000    2.0000
```

- 每个元素*2

```octave
>>2*ones(2,3)
ans =
   2   2   2
   2   2   2
```

- 高斯随机数

```octave
>>rand(3,3)
ans =
   0.851148   0.066648   0.422015
   0.843337   0.862546   0.983835
   0.602416   0.645067   0.096630
```

- 生成0矩阵

```octave
zeros(1,3)
```

- 单位矩阵

```octave
>>A = eye(3)
ans =
Diagonal Matrix
   1   0   0
   0   1   0
   0   0   1
```

- 读取

```octave
>>A(2,2) % 第2行第2列
ans =  1
>>A(:,2) % 第二列
ans =

   0
   1
   0

>>A(2,:) % 第二行
ans =

   0   1   0

>>A([1 2],:) % 第一行和第二行所有数据
ans =

   1   0   0
   0   1   0
   
>>A(:,2) = [10,11,12] % 将A第二列替换为[10;11;12]
A =

    1   10    0
    0   11    0
    0   12    1

>>A = [A, [100;101;102]] % 在A的最后加上一列：
A =

     1    10     0   100
     0    11     0   101
     0    12     1   102  
     
>>A(:) % 将A所有的元素合并成一个列向量
ans =

     1
     0
     0
    10
    11
    12
     0
     0
     1
   100
   101
   102
   
>>A = [1 2;3 4;5 6]
A =

   1   2
   3   4
   5   6

>>B = [7 8;9 10; 11 12]
B =

    7    8
    9   10
   11   12

>>c = [A B] % 行合并
c =

    1    2    7    8
    3    4    9   10
    5    6   11   12

>>D = [A;B] % 列合并
D =

    1    2
    3    4
    5    6
    7    8
    9   10
   11   12
```

## 2 移动数据

### 2.1 读取数据

- 加载数据

```octave
% 方式一：
>>load featuresX.dat
>>load priceY.dat
% 方式二：
>>load('featuresX.dat')
>>load('priceY.dat')
```

- 查看当前工作空间所有变量

```octave
who
% 更加详细的查看
whos
```

- 显示数据

```octave
>>featuresX
featuresX =
   2104      3
   1600      3
```

- 删除变量

```octave
clear featuresx
```

### 2.2 存储数据

```octave
>>v = priceY(1:10) % 取前十个元素
v =

   3999
   3299
   3690
   2320
   5399
   2999
   3149
   1989
   2120
   2425
% 存储
>>save hello.mat v
或者 save hello.mat v -ascii
```

## 3 计算数据

- 各种矩阵计算

  ```octave
  A * B
  A .* B
  A .^ 2
  1 ./ A
  log(A)
  sum(A)
  floor(A) # 向下取整
  ceil(A) # 向上取整
  ```

- 矩阵转置

  ```octave
  A'
  ```

- 向量中最大值(返回最大的值以及索引：从1开始)

  ```octave
  >>A = [1 2;3 4;5 6]
  A =
  
     1   2
     3   4
     5   6
  
  >>[val ind] = max(A)
  val =
  
     5   6
  
  ind =
  
     3   3
  ```

- 比较大小

  ```octave
  >>A > 3
  ans =
  
    0  0
    0  1
    1  1
  ```

- 找出特定元素

  ```octave
  find(A > 3)
  ```

- 找出矩阵中的特定元素

  ```octave
  A =
  
     1   2
     3   4
     5   6
  
  >>[r c] = find(A >= 3)
  r =
  
     2
     3
     2
     3
  
  c =
  
     1
     1
     2
     2
  ```

- 生成任意行、列、对角线和相等的矩阵

  ```octave
  magic(3)
  ```

- 构造一个由A,B两个矩阵中对应位置较大的数组成的矩阵

  ```octave
  >> A = [1 2;3 4; 5 6];
  >> B = [3 1;4 6; 2 9];
  >> max(A,B)
  
  ans =
  
       3     2
       4     6
       5     9
  ```

- 取出矩阵每列最大的元素

  ```octave
  >> max(A,[],1)
  
  ans =
  
       5     6
  ```

- 直接获得矩阵中最大的元素

  ```octave
  % 方式一：
  max(max(A))
  % 方式二：
  max(A(:))
  ```

- 矩阵的上下翻转

  ```octave
  >> eye(3)
  
  ans =
  
       1     0     0
       0     1     0
       0     0     1
  
  >> flipud(eye(3))
  
  ans =
  
       0     0     1
       0     1     0
       1     0     0
  ```

- 矩阵的逆

  ```octave
  >> A = rand(3,3)
  
  A =
  
      0.8147    0.9134    0.2785
      0.9058    0.6324    0.5469
      0.1270    0.0975    0.9575
  
  >> tmp = pinv(A)
  
  tmp =
  
     -1.9958    3.0630   -1.1690
      2.8839   -2.6919    0.6987
     -0.0291   -0.1320    1.1282
  ```

## 4 绘图数据

## 5 控制语句

- for循环

  ```matlab
  
  ```

  