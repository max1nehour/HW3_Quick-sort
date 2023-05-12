## HW3_Quick sort


## 程式碼與執行結果
* [程式碼github網址<hw2_quick_sort.ipynb>](https://github.com/max1nehour/HW2_hash_practice/blob/main/HW2_hash_practice.ipynb)

## 程式碼解析：

```py
def quick_sort(arr):
    if len(arr) <= 1:11
        return arr # 如果列表中只有一個元素或沒有元素，直接返回該列表
```
* 串列生成式：結合迴圈與條件測試式，以減少繁瑣的語法
* 舉例：odd = [number for number in range(1,10) if number % 2 == 1]
```py
    else:
        pivot = arr[0] # 設定基準點為列表第一個元素
        less = [x for x in arr[1:] if x <= pivot] # 小於等於基準點的元素
        greater = [x for x in arr[1:] if x > pivot] # 大於基準點的元素
```    

# 顯示排序過程
```py
        print("pivot: ", pivot)
        print("less: ", less)
        print("greater: ", greater)
        return quick_sort(less) + [pivot] + quick_sort(greater) # 進行遞迴排序，直到所有元素都排序完成
``` 
```py
# 測試程式碼
arr = [33, 67, 8, 13, 54, 119, 3, 84, 25, 41]
print("Original array: ", arr)
sorted_arr = quick_sort(arr)
print("Sorted array: ", sorted_arr)
```

