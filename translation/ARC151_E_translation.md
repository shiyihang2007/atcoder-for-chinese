## 题意 

已知一个长度为 $N$ 的序列 $A=(A_1,A_2,...,A_N)$，以及两个长度分别为 $P,Q$ 的 $A$ 的子序列 $X=(X_1,X_2,...,X_P),Y=(Y_1,Y_2,...,Y_Q)$。

可以对于 $X$ 进行以下操作任意次。

- 在 $X$ 开头加上一个数。
- 删去 $X$ 开头第一个数。
- 在 $X$ 结尾加上一个数。
- 删去 $X$ 最后一个数。

$X$ 每次操作后都需要保证是**非空**的并且是 $A$ 的子序列，求出最小操作数使得 $X=Y$，保证有解。

## 数据范围

- $1\le N\le 2\times 10^5$
- $1\le A_i\le N$
- $1\le P,Q\le N$
- $X,Y$ 都是 $A$ 的子序列。

## 输入格式

第一行一个数 $N$。

第二行 $N$ 个数，表示 $A$。

第三行一个数 $P$。

第四行 $P$ 个数，表示 $X$。

第五行一个数 $Q$。

第六行 $Q$ 个数，表示 $Y$。

## 输出格式

一行一个数，表示答案。

## 样例

### 样例输入1

```
7
3 1 4 1 5 7 2
2
3 1
3
1 5 7
```

### 样例输出1

```
3
```

### 样例解释1

对 $X$ 进行以下操作：

- 删去 $X$ 开头，变成 $X=(1)$。
- 在 $X$ 结尾加上 $5$ ，变成 $X=(1,5)$。
- 在 $X$ 结尾加上 $7$，变成 $X=(1,5,7)$。

这是操作数最小的方案。

### 样例输入2

```
20
2 5 1 2 7 7 4 5 3 7 7 4 5 5 5 4 6 5 6 1
6
1 2 7 7 4 5
7
7 4 5 5 5 4 6
```

### 样例输出2

```
7
```
