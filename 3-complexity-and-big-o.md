# 3-10 the idea of algorithm

## 演算法優劣分析

兩個方式分析演算法好壞，利用 complexity，分別為時間複雜度與空間複雜度

## what is algorithm

-   Algorithm is a finite sequence of well-defined,computer-implementable instructions,typically to solve a class of problems or perform a computations.
    演算法是定義明確的計算機可實現指令的有限序列，通常用於解決一類問題或執行計算。

-   Easily speaking, algorithm is a step-by-step procedure to solve a problems
    簡單地說，算法是解決問題的一步一步的過程

## 11. Comparing Algoriindehms

算階級相加

```javascript
///input n output sum(1~n)
// sum1 vs sum2
const fun1 = (n) => {
    const result = 0
    for (let i = 0; i <= n; i++) {
        result + i
    }
    return result
}

const fun2 = (n) => ((1 + n) * n) / 2//利用梯形公式算出答案
```

同樣解決一個問題
fun2 所用時間明顯小於 sum1

## 12 Complexity

分析複雜度可以分為時間複雜度與空間複雜度

## Analysis of fun1 and fun2

```javascript
const fun1 = (n) => {
    const result = 0 //operation 1
    for (let i = 0; i <= n; i++) {
        result + i
    } //operation 2
    return result
}
```

## 1.fun1 的複雜度

fun1 總共三個 operations 且 n 次 為 3 f(n)=3n

```javascript
const fun1 = (n) => {
    const result = 0 //operation 1
    for (let i = 0; i <= n; i++) {
        result + i
    } //operation 2
    return result
}
```

## 2. fun2 的複雜度

fun2 總共三個 operations 為 3 f(n)=3

```javascript
const fun2 = (n) => ((1 + n) * n) / 2
```

# 14 Big O Notation

## What is Big O Natation ?

-   Big O Notation is a tool that describe the limiting behavior of a function when the argument tends towards a particular value of infinity.
-   Big O Notation 是一種工具，用於描述當參數趨向於某個特定的無窮大值時函數的限制行為。

-   Big O Notation has a worst case scenario, which means it shows the general trends of complexity when the size of inputs is extremely large.
-   Big O Notation 有一個最壞的情況，這意味著當輸入的大小非常大時，它顯示了複雜性的趨勢。

## Calculating Big O Value

### 定義

1. Constant does't matter //常數不重要
   f(n) = 3n 在此函數中，n 為變數，3 為常數
   f(n) = 3n => O(3n) => O(n)
2. Small Terms don't matter // 小的不重要
   f(n) = 3n^2 +6n +4 => O(3n^2)=> O(n^2)

3. Logarithm base does't matter// log 底數不重要
   f(n) = log 2^n => O(log n)

### 練習

f(n) = 2n
=> O(n) #
f(n) = 13n^3 +6n +7
=> O(n^3) #
f(n) = 4 log2 n
=> O(log n)
f(n) = 5
=> O(1)

### 常見 越上面的，複雜度越低

1. O(1)
2. O(log n)
3. O(n)
4. O(nlog)
5. O(n^2)
6. O(n^3)

# 15 Understand Big O
分析以下四個function 複雜度
```typescript
f1(n)=()=>1000   //O(1)
f2(n)=()=>n      //O(n)
f3(n)=()=>n+1000 //O(n)
f4(n)=()=>n*n    //O(n^2)
```
思考：f2 與f3 相比，f3多了加1000的動作，但為何複雜度計算時卻和f2是一樣的？

答案：Big Ｏ討論worst case，當input n 越大， f2 與 f3 中，f3 中的常數對複雜度越不重要。

# 16 Understand Big O Notation
## 待補充

# 17 Big Omega And Big Theta
## 待補充

# 18 Big O in Arrays And Objects
分析 js 中 Object and Array BigO

|        | Insertion             | Removal            | Searching | Acccessing |
|--------|-----------------------|--------------------|-----------|------------|
| Object | O(1)                  | O(1)               | O(n)      | O(1)       |
|  Array | push:O(1) unShif:O(n) | pop:O(1) shif:O(n) | O(n)      | O(1)       |
|        |                       |                    |           |            |


