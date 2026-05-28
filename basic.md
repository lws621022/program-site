---
layout: default
title: 基本觀念
---

# Python 基本觀念

針對 Python 的各種觀念、函式等。了解這些對學科、術科有很大的幫助。

內容為 PDF 檔，方便同學下載或列印出來隨時查看。

基本觀念：[檔案下載](files/basic.pdf)

---

## Python 資料型態線上教學資源

Python 資料型態線上教學資源，針對不熟悉的資料型態要多了解用法。

- [Python str](https://shengyu7697.github.io/python-str/)：字串用法與範例 線上教學網站
- [Python list](https://shengyu7697.github.io/python-list/)：串列用法與範例 線上教學網站
- [Python set](https://shengyu7697.github.io/python-set/)：集合用法與範例 線上教學網站
- [Python dict](https://shengyu7697.github.io/python-dict/)：字典用法與範例 線上教學網站

---

## 重點新增

部分資料更新時記錄於此。

---

## 進階觀念：defaultdict

`defaultdict` 是 `dict` 的變形，具有自動初始化的特性。

如果訪問的鍵不存在，會自動建立並設為預設值，減少手動檢查鍵是否存在的麻煩。

```python
from collections import defaultdict

words = ["apple", "ant", "banana", "bat"]
group = defaultdict(list)

for word in words:
    # 不需檢查 key 是否存在
    group[word[0]].append(word)

print(group)
# {'a': ['apple', 'ant'], 'b': ['banana', 'bat']}
```

---

## 進階觀念：Counter

`Counter` 可以快速統計元素出現的次數，常用在字串、串列、統計題型中。

```python
from collections import Counter

# 使用者輸入句子
sentence = input("請輸入一個英文句子：")

# 去空白
n_s = sentence.replace(" ", "")

# 統計字母出現次數
letter_counts = Counter(n_s)

# 輸出結果
for letter, count in sorted(letter_counts.items()):
    print(f"{letter}: {count}")
```
