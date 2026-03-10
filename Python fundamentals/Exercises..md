
Two sums

```python
def twoSum(self, nums: List[int], target: int) -> List[int]:():
    # Sử dụng f-string hiện đại
    find = {}
    for i, n in enumerate(nums):
		complement = target - n
		if i in find:
			return [find[complement], i]
		find[n] = i
	return 
```


> [!info] Giải thích `enumerate()`
> Hàm này trả về một đối tượng liệt kê. Nó giúp bạn lấy cả **index** và **value** cùng lúc.
> - **Index**: Vị trí phần tử.
> - **Value**: Giá trị thực tế.

Longest common prefix

```python
def longestCommonPrefix(self, strs: List[str]) -> str:

	result = "" ## tạo 1 string rỗng

	for i in range(len(strs[0])): # Xét qua chuỗi đầu tiên strs[0] và duyệt qua từng vị trí kí tự của nó. 

		for s in strs: # với mỗi vị trí i. Cần duyệt qua tất cả các chuỗi còn lại trong danh sách

			if i == len(s) or s[i] != strs[0][i]: # nếu vi phạm việc chỉ số hiện tại i chạm đến độ dài của một chuỗi hoặc kí tự tại ví trí i khác với kí tự chuẩn của chuỗi đầu tiên

				return result # quay về result

		result += strs[0][i] #Nếu vượt qua được vòng lặp bên trong (nghĩa là tất cả các chuỗi đều có ký tự giống nhau ở vị trí `i`), bạn dùng **lệnh gán tăng cường** để nối ký tự đó vào chuỗi kết quả `result`

	return result
```

Write a short Python function, is multiple(n, m), that takes two integer
values and returns True if n is a multiple of m, that is, n = mi for some
integer i, and False otherwise.
```python

def is_multiplel(n, m):
	if n % m == 0:
		return True
	else:
		return False
print(is_multiple(10, 2))
	
	
```