# VPython-03

🐍 課程說明
- 主題：Python 列表（List）與基本操作教學
- 目標：理解列表（List）的基本特性

在學習完基礎的變數類型（str, int, float, bool）之後，下一步會進入到 Python 的集合數據類型 (Collection Data Types)，這是 Python 強大的核心功能之一。

List 為最常用且功能最多的數據結構。

1. 什麼是列表 (List)？  
概念： 列表是用來儲存多個項目的單一變數。

特性：
- 有序 (Ordered)： 項目有固定的順序，順序不會改變。
- 可變 (Mutable)： 建立後可以修改、新增或刪除項目。
- 允許重複 (Allows Duplicates)： 列表中可以有多個相同值的項目。
- 混合類型 (Heterogeneous)： 列表可以包含不同數據類型（int, str, bool 等）的項目。

語法： 使用 中括號 [] 來建立列表，項目之間用逗號 , 分隔。

2. 建立列表（範例）
```Python
# 範例 1: 數字列表
scores = [95, 88, 70, 92]
print(scores)

# 範例 2: 字符串列表
fruits = ["apple", "banana", "cherry"]
print(fruits)

# 範例 3: 混合類型列表
mixed_list = [10, "hello", True, 3.14]
print(mixed_list)
```

3. 存取列表元素：索引 (Indexing)  
列表的項目是從 0 開始編號的 (稱為索引/Index)。  
使用 中括號 [] 和索引號來存取特定的項目。  

負數索引： 使用負數索引可以從列表的末尾開始計算（-1 代表最後一個項目）。

```Python

fruits = ["apple", "banana", "cherry", "orange"]

# 取得第一個項目 (索引 0)
print(fruits[0])  # 輸出: apple

# 取得第三個項目 (索引 2)
print(fruits[2])  # 輸出: cherry

# 取得最後一個項目 (索引 -1)
print(fruits[-1]) # 輸出: orange
```

4. 基本列表操作
4.1. 修改 (Change)  
使用索引來重新賦值，改變列表中的特定項目。

```Python

fruits = ["apple", "banana", "cherry"]
# 將 "banana" 改為 "grape"
fruits[1] = "grape"
print(fruits)  # 輸出: ['apple', 'grape', 'cherry']
```

4.2. 新增 (Add)  
list.append(item)：在列表的 末尾 添加一個新項目。  
list.insert(index, item)：在指定的 索引位置 插入一個新項目。

```Python

fruits = ["apple", "banana"]
fruits.append("kiwi")     # 在末尾新增
print(fruits)  # 輸出: ['apple', 'banana', 'kiwi']

fruits.insert(1, "grape") # 在索引 1 處插入
print(fruits)  # 輸出: ['apple', 'grape', 'banana', 'kiwi']
```

4.3. 刪除 (Remove)  
list.remove(item)：移除 列表中 第一個 匹配到的項目。  
list.pop(index)：移除 並 返回 指定索引位置的項目 (若不指定索引，則移除並返回最後一個)。  
del list[index]：刪除 指定索引位置的項目。

```Python

fruits = ["apple", "banana", "kiwi", "banana"]
fruits.remove("banana") # 移除第一個 "banana"
print(fruits) # 輸出: ['apple', 'kiwi', 'banana']

removed_item = fruits.pop(0) # 移除並取出索引 0 的項目
print(removed_item) # 輸出: apple
print(fruits)       # 輸出: ['kiwi', 'banana']

del fruits[0] # 刪除索引 0 的項目 ("kiwi")
print(fruits) # 輸出: ['banana']
```

5. 實用內建函數  
len(list)：計算列表中的項目數量。

```Python

my_list = [10, 20, 30]
print(len(my_list)) # 輸出: 3
```

💡 實戰練習  
任務： 請建立一個名為 to_do_list 的列表，其中包含 3-5 個待辦事項（字符串）。

步驟：
1. 印出完整的 to_do_list。
2. 使用索引取得並印出第一個待辦事項。
3. 使用 append() 新增一個事項。
4. 將列表中的某個舊事項用修改的方式更新為新事項。
5. 使用 remove() 移除一個已完成的事項。
