## HW3_Quick sort

# 讀取txt檔 並運用hash計算有幾種不同的單字和其出現次數

## 程式碼與執行結果
* [程式碼github網址<hw2_hash_practice.ipynb>](https://github.com/max1nehour/HW2_hash_practice/blob/main/HW2_hash_practice.ipynb)

## 程式碼解析：

```py
def quick_sort(arr):
    if len(arr) <= 1:11
        return arr # 如果列表中只有一個元素或沒有元素，直接返回該列表
    else:
        pivot = arr[0] # 設定基準點為列表第一個元素
        less = [x for x in arr[1:] if x <= pivot] # 小於等於基準點的元素
        greater = [x for x in arr[1:] if x > pivot] # 大於基準點的元素
        
        
        # 在排序過程中顯示過程
        print("pivot: ", pivot)
        print("less: ", less)
        print("greater: ", greater)
        return quick_sort(less) + [pivot] + quick_sort(greater) # 進行遞迴排序，直到所有元素都排序完成

# 測試程式碼
arr = [33, 67, 8, 13, 54, 119, 3, 84, 25, 41]
print("Original array: ", arr)
sorted_arr = quick_sort(arr)
print("Sorted array: ", sorted_arr)
```

