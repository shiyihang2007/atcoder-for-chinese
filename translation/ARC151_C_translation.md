## 题意 

有 $N$ 个方格排成一排，被标号为方格 $1$，方格 $2$，... ，方格 $N$，对于 $1\le i < N$，方格 $i$ 与 方格 $i+1$ 相邻。

初始时，有 $M$ 个方格上写着 $0$ 或者 $1$，对于 $i(1\le i\le M)$，方格 $X_i$ 上写着 $Y_i$，其余方格为空。

高桥和青木进行一个游戏，两个人轮流进行以下操作，高桥先手。

- 选择一个空方格，在上面写上 $0$ 或者 $1$，需要保证任意相邻两个方格不能写有相同的数字。

第一个不能操作的人输，另一个人赢。

双方都用最优策略，判断谁能赢。

## 数据范围

- $1\le N\le 10^{18}$
- $0\le M\le \min\{ N,2\times 10^5 \}$
- $1\le X_1 < X_2 < \cdots < X_M \le N$
- $Y_i\in \{0,1\}$
- 初始没有相邻两个格子写有相同的数。

## 输入格式

第一行两个数 $N,M$。

接下来 $M$ 行，每行两个数，表示 $X_i,Y_i$。

## 输出格式

如果高桥赢，输出 `Takahashi`，青木赢输出 `Aoki`。

## 样例

### 样例输入1

```
7 2
2 0
4 1
```

### 样例输出1

```
Takahashi
```

### 样例解释1

以下是一个可能的游戏过程：

1. 高桥在方格 $6$ 上写 $0$。
2. 青木在方格 $1$ 上写 $1$。
3. 高桥在方格 $7$ 上写 $1$。

此时青木无法操作，高桥获胜。

### 样例输入2

```
3 3
1 1
2 0
3 1
```

### 样例输出2

```
Aoki
```

### 样例解释2

开始就无法操作，青木赢。

### 样例输入3

```
1000000000000000000 0
```

### 样例输出3

```
Aoki
```