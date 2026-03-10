
## 1. Xử lý cơ bản với String

  

| **Hàm**                             | **Chức năng**                                                                | **Ví dụ**                                                        |
| ----------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------- |
| `len()`                             | Lấy độ dài chuỗi.                                                            | `len("hello")` → `5`                                             |
| `str()`                             | Chuyển đổi dữ liệu khác thành chuỗi.                                         | `str(123)` → `"123"`                                             |
| `lower()`                           | Chuyển chuỗi thành chữ thường.                                               | `"HELLO".lower()` → `"hello"`                                    |
| `upper()`                           | Chuyển chuỗi thành chữ hoa.                                                  | `"hello".upper()` → `"HELLO"`                                    |
| `capitalize()`                      | Viết hoa chữ cái đầu tiên của chuỗi.                                         | `"python".capitalize()` → `"Python"`                             |
| `title()`                           | Viết hoa chữ cái đầu của mỗi từ trong chuỗi.                                 | `"hello world".title()` → `"Hello World"`                        |
| `strip()`                           | Xóa khoảng trắng ở đầu và cuối chuỗi.                                        | `"  hello  ".strip()` → `"hello"`                                |
| `lstrip()`/`rstrip()`               | Xóa khoảng trắng ở đầu (`lstrip`) hoặc cuối chuỗi (`rstrip`).                | `"  hello  ".lstrip()` → `"hello  "`                             |

  

---

  

## 2. Tìm kiếm và thay thế

  

| **Hàm**            | **Chức năng**                                                                  | **Ví dụ**                                                        |
| ------------------ | ------------------------------------------------------------------------------ | ---------------------------------------------------------------- |
| `find()`           | Tìm vị trí đầu tiên của một chuỗi con.                                         | `"hello world".find("world")` → `6`                              |
| `rfind()`          | Tìm vị trí cuối cùng của một chuỗi con.                                        | `"hello world world".rfind("world")` → `12`                      |
| `index()`          | Tương tự `find()`, nhưng báo lỗi nếu không tìm thấy.                           | `"hello".index("l")` → `2`                                       |
| `replace()`        | Thay thế chuỗi con bằng chuỗi khác.                                            | `"hello world".replace("world", "Python")` → `"hello Python"`    |
| `count()`          | Đếm số lần xuất hiện của một chuỗi con.                                        | `"hello world".count("o")` → `2`                                 |
| `startswith()`     | Kiểm tra chuỗi có bắt đầu bằng một chuỗi con không.                            | `"hello".startswith("he")` → `True`                              |
| `endswith()`       | Kiểm tra chuỗi có kết thúc bằng một chuỗi con không.                           | `"hello".endswith("lo")` → `True`                                |

  

---

  

## 3. Phân tách và nối chuỗi

  

| **Hàm**                 | **Chức năng**                                                                   | **Ví dụ**                                                       |
| ----------------------- | ------------------------------------------------------------------------------- | --------------------------------------------------------------- |
| `split()`               | Tách chuỗi thành danh sách dựa trên ký tự (mặc định là khoảng trắng).           | `"a,b,c".split(",")` → `['a', 'b', 'c']`                        |
| `rsplit()`              | Tách chuỗi từ cuối đến đầu.                                                     | `"a,b,c".rsplit(",", 1)` → `['a,b', 'c']`                       |
| `splitlines()`          | Tách chuỗi thành danh sách dựa trên ký tự xuống dòng (`\n`).                    | `"line1\nline2".splitlines()` → `['line1', 'line2']`            |
| `join()`                | Nối các phần tử trong danh sách thành chuỗi với ký tự ngăn cách.                | `",".join(['a', 'b', 'c'])` → `"a,b,c"`                         |

  

---

  

## 4. Căn chỉnh chuỗi

  

| **Hàm**             | **Chức năng**                                                                  | **Ví dụ**                                                       |
| ------------------- | ------------------------------------------------------------------------------ | --------------------------------------------------------------- |
| `center()`          | Căn giữa chuỗi với chiều dài và ký tự đệm.                                     | `"hello".center(10, "*")` → `"**hello**"`                       |
| `ljust()`           | Căn trái chuỗi với chiều dài và ký tự đệm.                                     | `"hello".ljust(10, "*")` → `"hello*****"`                       |
| `rjust()`           | Căn phải chuỗi với chiều dài và ký tự đệm.                                     | `"hello".rjust(10, "*")` → `"*****hello"`                       |
| `zfill()`           | Thêm số `0` vào đầu chuỗi đến khi đạt chiều dài mong muốn.                     | `"42".zfill(5)` → `"00042"`                                     |

  

---

  

## 5. Kiểm tra thuộc tính chuỗi

  

| **Hàm**             | **Chức năng**                                                        | **Ví dụ**                                                        |
| ------------------- | -------------------------------------------------------------------- | ---------------------------------------------------------------- |
| `isalpha()`         | Kiểm tra chuỗi chỉ chứa chữ cái.                                     | `"abc".isalpha()` → `True`                                       |
| `isdigit()`         | Kiểm tra chuỗi chỉ chứa số.                                          | `"123".isdigit()` → `True`                                       |
| `isalnum()`         | Kiểm tra chuỗi chỉ chứa chữ cái hoặc số.                             | `"abc123".isalnum()` → `True`                                    |
| `islower()`         | Kiểm tra tất cả ký tự trong chuỗi là chữ thường.                     | `"abc".islower()` → `True`                                       |
| `isupper()`         | Kiểm tra tất cả ký tự trong chuỗi là chữ hoa.                        | `"ABC".isupper()` → `True`                                       |
| `isspace()`         | Kiểm tra chuỗi chỉ chứa khoảng trắng.                                | `"   ".isspace()` → `True`                                       |
| `istitle()`         | Kiểm tra chuỗi có phải dạng tiêu đề (chữ cái đầu mỗi từ viết hoa).   | `"Hello World".istitle()` → `True`                               |

  

---

  

## 6. Biến đổi chuỗi

  

| **Hàm**            | **Chức năng**                                                              | **Ví dụ**                                                       |
| ------------------ | -------------------------------------------------------------------------- | --------------------------------------------------------------- |
| `swapcase()`       | Đổi chữ hoa thành chữ thường và ngược lại.                                 | `"Hello".swapcase()` → `"hELLO"`                                |
| `casefold()`       | Chuyển chuỗi thành dạng viết thường để so sánh không phân biệt hoa thường. | `"Straße".casefold()` → `"strasse"`                             |
| `translate()`      | Thay thế ký tự dựa trên bảng dịch.                                         | `"hello".translate(str.maketrans("h", "H"))` → `"Hello"`        |

  

---

  

# Regex trong Python

  

## 1. Các hàm chính trong module `re`

  

### **1. `split()`**

- **Công dụng**: Tách chuỗi dựa trên một biểu thức chính quy.

- **Cú pháp**:

  ```python

  re.split(pattern, string, maxsplit=0, flags=0)

  ```

- **Tham số chính**:

  - `pattern`: Biểu thức chính quy dùng để tách.

  - `string`: Chuỗi cần tách.

  - `maxsplit` (tùy chọn): Số lần tách tối đa (mặc định là không giới hạn).

  

- **Ví dụ**:

  ```python

  import re

  text = "word1, word2; word3.word4"

  result = re.split(r'[,\.;\s]+', text)

  print(result)  # ['word1', 'word2', 'word3', 'word4']

  ```

  

---

  

### **2. `findall()`**

- **Công dụng**: Trả về tất cả các kết quả khớp (là danh sách) trong chuỗi.

- **Cú pháp**:

  ```python

  re.findall(pattern, string, flags=0)

  ```

- **Ví dụ**:

  ```python

  import re

  text = "Python is great. Python is easy to learn."

  result = re.findall(r'Python', text)

  print(result)  # ['Python', 'Python']

  ```

  

---

  

### **3. `search()`**

- **Công dụng**: Tìm kiếm **lần xuất hiện đầu tiên** của mẫu regex trong chuỗi.

- **Cú pháp**:

  ```python

  re.search(pattern, string, flags=0)

  ```

- **Trả về**: Một đối tượng `Match` hoặc `None` nếu không tìm thấy.

  

- **Ví dụ**:

  ```python

  import re

  text = "The rain in Spain"

  match = re.search(r'rain', text)

  if match:

      print(f"Found '{match.group()}' at position {match.start()}-{match.end()}")

  ```

  

---

  

### **4. `match()`**

- **Công dụng**: Kiểm tra xem chuỗi có khớp với biểu thức chính quy bắt đầu từ vị trí đầu tiên không.

- **Cú pháp**:

  ```python

  re.match(pattern, string, flags=0)

  ```

- **Ví dụ**:

  ```python

  import re

  text = "Python is fun"

  match = re.match(r'Python', text)

  if match:

      print(f"Matched: {match.group()}")

  ```

  

---

  

### **5. `sub()`**

- **Công dụng**: Thay thế các chuỗi khớp với mẫu regex bằng một chuỗi khác.

- **Cú pháp**:

  ```python

  re.sub(pattern, repl, string, count=0, flags=0)

  ```

- **Ví dụ**:

  ```python

  import re

  text = "I love Python. Python is amazing."

  result = re.sub(r'Python', 'Regex', text)

  print(result)  # "I love Regex. Regex is amazing."

  ```

  

---

  

### **6. `finditer()`**

- **Công dụng**: Tìm tất cả các kết quả khớp và trả về một **iterator** chứa các đối tượng `Match`.

- **Cú pháp**:

  ```python

  re.finditer(pattern, string, flags=0)

  ```

- **Ví dụ**:

  ```python

  import re

  text = "Python Python Python"

  matches = re.finditer(r'Python', text)

  for match in matches:

      print(f"Found '{match.group()}' at position {match.start()}-{match.end()}")

  ```

  

---

  

### **7. `start()` và `end()`**

- **Công dụng**: Xác định vị trí bắt đầu (`start()`) và kết thúc (`end()`) của mẫu khớp trong chuỗi.

- **Ví dụ**:

  ```python

  import re

  text = "Hello world"

  match = re.search(r'world', text)

  if match:

      print(f"Start: {match.start()}, End: {match.end()}")  # Start: 6, End: 11

  ```

  

---

  

### **8. `group()`**

- **Công dụng**: Lấy chuỗi con khớp với regex trong đối tượng `Match`.

- **Ví dụ**:

  ```python

  import re

  text = "My email is example@gmail.com"

  match = re.search(r'[\w\.-]+@[\w\.-]+', text)

  if match:

      print(match.group())  # example@gmail.com

  ```

  

---

  

### **9. `compile()`**

- **Công dụng**: Biên dịch biểu thức chính quy để tái sử dụng nhiều lần.

- **Cú pháp**:

  ```python

  regex = re.compile(pattern, flags=0)

  ```

- **Ví dụ**:

  ```python

  import re

  pattern = re.compile(r'Python')

  text = "Python is awesome. Python is fun."

  matches = pattern.findall(text)

  print(matches)  # ['Python', 'Python']

  ```

  

---

  

## 2. Ký tự đặc biệt trong Regex

  

### **1. Ký tự đại diện và khớp**

| **Ký tự**  | **Ý nghĩa**                                                   | **Ví dụ**                                | **Kết quả**                      |
| ---------- | ------------------------------------------------------------- | ---------------------------------------- | -------------------------------- |
| `.`        | Đại diện cho **bất kỳ ký tự nào** ngoại trừ xuống dòng (`\n`) | `re.findall(r'a.b', 'acb adb abb a_b')`  | `['acb', 'adb', 'a_b']`          |
| `\d`       | Khớp với **chữ số** (0–9)                                     | `re.findall(r'\d', 'abc123def')`         | `['1', '2', '3']`                |
| `\D`       | Khớp với **bất kỳ ký tự nào không phải chữ số**               | `re.findall(r'\D', 'abc123def')`         | `['a', 'b', 'c', 'd', 'e', 'f']` |
| `\w`       | Khớp với **ký tự chữ cái, số, hoặc `_`**                      | `re.findall(r'\w+', 'Hello_World! 123')` | `['Hello_World', '123']`         |
| `\W`       | Khớp với **bất kỳ ký tự nào không phải chữ cái, số hoặc `_`** | `re.findall(r'\W+', 'Hello_World! 123')` | `[' ', '! ', ' ']`               |
| `\s`       | Khớp với **khoảng trắng** (space, tab, newline)               | `re.findall(r'\s', 'Hello World\n123')`  | `[' ', '\n']`                    |
| `\S`       | Khớp với **bất kỳ ký tự nào không phải khoảng trắng**         | `re.findall(r'\S+', 'Hello World\n123')` | `['Hello', 'World', '123']`      |

  

---

  

### **2. Ký tự neo (Anchors)**

| **Ký tự**  | **Ý nghĩa**                          | **Ví dụ**                                  | **Kết quả** |
| ---------- | ------------------------------------ | ------------------------------------------ | ----------- |
| `^`        | Khớp với **đầu chuỗi**               | `re.findall(r'^Hello', 'Hello World')`     | `['Hello']` |
| `$`        | Khớp với **cuối chuỗi**              | `re.findall(r'World$', 'Hello World')`     | `['World']` |
| `\B`       | Khớp với **không phải biên giới từ** | `re.findall(r'lo\B', 'Hello World')`       | `['lo']`    |
| `\b`       | Khớp với **biên giới từ**            | `re.findall(r'\bWorld\b', 'Hello World!')` | `['World']` |

---
### **3. Ký tự định lượng (Quantifiers)**

| **Ký tự**  | **Ý nghĩa**               | **Ví dụ**                          | **Kết quả**              |
| ---------- | ------------------------- | ---------------------------------- | ------------------------ |
| `*`        | Khớp **0 hoặc nhiều lần** | `re.findall(r'a*', 'aaabaaa')`     | `['aaa', '', 'aaa', '']` |
| `+`        | Khớp **1 hoặc nhiều lần** | `re.findall(r'a+', 'aaabaaa')`     | `['aaa', 'aaa']`         |
| `?`        | Khớp **0 hoặc 1 lần**     | `re.findall(r'ab?', 'abbbabc')`    | `['ab', 'ab']`           |
| `{n}`      | Khớp chính xác **n lần**  | `re.findall(r'a{3}', 'aaabaaa')`   | `['aaa']`                |
| `{n,}`     | Khớp **ít nhất n lần**    | `re.findall(r'a{2,}', 'aaabaaa')`  | `['aaa', 'aaa']`         |
| `{n,m}`    | Khớp từ **n đến m lần**   | `re.findall(r'a{2,3}', 'aaabaaa')` | `['aaa', 'aaa']`         |

  

---

  

### **4. Nhóm và lựa chọn (Grouping and Alternation)**

| **Ký tự** | **Ý nghĩa**           | **Ví dụ**                              | **Kết quả**      |
| --------- | --------------------- | -------------------------------------- | ---------------- |
| `()`      | Nhóm mẫu lại với nhau | `re.findall(r'(ab)+', 'ababababc')`    | `['ab', 'ab']`   |
| `\|`      | Khớp với **hoặc**     | `re.findall(r'cat dog','cat and dog')` | `['cat', 'dog']` |

---

### **5. Ký tự thoát (Escape Characters)**

| Ký tự | Ý nghĩa | Ví dụ | Kết quả |
|---|---|---|---|
| `\.` | Khớp với dấu chấm thực | `re.findall(r'\.', 'example.com')` | `['.']` |
| `\\` | Khớp với dấu gạch chéo ngược thực | `re.findall(r'\\', r'c:\\path')` | `['\\']` |
  

---

  

### **6. Ký tự khớp nhóm (Character Classes)**

| **Ký tự**  | **Ý nghĩa**                                           | **Ví dụ**                                | **Kết quả**                                |
| ---------- | ----------------------------------------------------- | ---------------------------------------- | ------------------------------------------ |
| `[abc]`    | Khớp với **a, b, hoặc c**                             | `re.findall(r'[aeiou]', 'hello world')`  | `['e', 'o', 'o']`                          |
| `[^abc]`   | Khớp với **bất kỳ ký tự nào không phải a, b, hoặc c** | `re.findall(r'[^aeiou]', 'hello world')` | `['h', 'l', 'l', ' ', 'w', 'r', 'l', 'd']` |
| `[a-z]`    | Khớp với **các ký tự từ a đến z**                     | `re.findall(r'[a-z]', 'Hello123')`       | `['e', 'l', 'l', 'o']`                     |
| `[A-Z]`    | Khớp với **các ký tự từ A đến Z**                     | `re.findall(r'[A-Z]', 'Hello123')`       | `['H']`                                    |
| `[0-9]`    | Khớp với **các số từ 0 đến 9**                        | `re.findall(r'[0-9]', 'Hello123')`       | `['1', '2', '3']`                          |

  

---

  

### **7. Các mẫu đặc biệt**

| **Ký tự**          | **Ý nghĩa**                           | **Ví dụ**                               | **Kết quả**                 |
| ------------------ | ------------------------------------- | --------------------------------------- | --------------------------- |
| `(?i)`             | Bỏ qua phân biệt chữ hoa/thường       | `re.findall(r'(?i)hello', 'Hello')`     | `['Hello']`                 |
| `(?<=x)`           | Khớp với chuỗi ngay **sau** `x`       | `re.findall(r'(?<=\$)\d+', '$10 $20')`  | `['10', '20']`              |
| `(?=x)`            | Khớp với chuỗi ngay **trước** `x`     | `re.findall(r'\d+(?=%)', '50% 100%')`   | `['50', '100']`             |
| `(?!x)`            | Không khớp với chuỗi ngay **sau** `x` | `re.findall(r'\d+(?!%)', '50% 100 kg')` | `['100']`                   |

  

---

  

# Dictionary trong Python

  

## 1. Khởi tạo dictionary

| **Cách khởi tạo**     | **Mô tả**                                                                                  | **Ví dụ**                                                        |                             |
| --------------------- | ------------------------------------------------------------------------------------------ | ---------------------------------------------------------------- | --------------------------- |
| Sử dụng `{}`          | Khởi tạo dictionary rỗng hoặc có giá trị.                                                  | `my_dict = {"a": 1, "b": 2}`                                     |                             |
| Sử dụng `dict()`      | Khởi tạo dictionary bằng hàm `dict()`.                                                     | `my_dict = dict(a=1, b=2)`                                       |                             |
| Từ danh sách tuple    | Chuyển đổi danh sách tuple thành dictionary.                                               | `my_dict = dict([("a", 1), ("b", 2)])`                           |                             |
| Sử dụng comprehension | Tạo dictionary từ vòng lặp.                                                                | `my_dict = {x: x**2 for x in range(5)}`                          | )}`                         |

  

---

  

## 2. Các thao tác cơ bản với dictionary

  

| **Cú pháp/Hàm**        | **Chức năng**                                                                    | **Ví dụ**                                                        |
| ---------------------- | -------------------------------------------------------------------------------- | ---------------------------------------------------------------- |
| `my_dict[key]`         | Truy cập giá trị dựa trên key.                                                   | `my_dict["a"]` → `1`                                             |
| `my_dict[key] = value` | Gán giá trị cho key.                                                             | `my_dict["c"] = 3` → `{'a': 1, 'b': 2, 'c': 3}`                  |
| `del my_dict[key]`     | Xóa một key-value trong dictionary.                                              | `del my_dict["a"]`                                               |
| `key in my_dict`       | Kiểm tra key có tồn tại trong dictionary không.                                  | `'a' in my_dict` → `True`                                        |
| `len(my_dict)`         | Trả về số lượng key-value trong dictionary.                                      | `len(my_dict)` → `2`                                             |
| `my_dict.clear()`      | Xóa toàn bộ các phần tử trong dictionary.                                        | `my_dict.clear()` → `{}`                                         |

---

## 3. Các phương thức xử lý dictionary

  

| **Phương thức**           | **Chức năng**                                                                   | **Ví dụ**                                                       |
| ------------------------- | ------------------------------------------------------------------------------- | --------------------------------------------------------------- |
| `get(key, default)`       | Lấy giá trị của key, trả về giá trị mặc định nếu key không tồn tại.             | `my_dict.get("a", 0)` → `1`                                     |
| `pop(key, default)`       | Lấy giá trị của key và xóa nó khỏi dictionary.                                  | `my_dict.pop("a")` → `{'b': 2}`                                 |
| `popitem()`               | Xóa và trả về một cặp key-value bất kỳ.                                         | `my_dict.popitem()` → `('b', 2)`                                |
| `setdefault(key, value)`  | Trả về giá trị của key, nếu không tồn tại sẽ thêm key với giá trị mặc định.     | `my_dict.setdefault("c", 3)` → `{'a': 1, 'b': 2, 'c': 3}`       |
| `update(other_dict)`      | Thêm hoặc cập nhật dictionary từ một dictionary hoặc iterable khác.             | `my_dict.update({"d": 4})` → `{'a': 1, 'b': 2, 'd': 4}`         |

  

---

  

## 4. Duyệt các phần tử trong dictionary

  

| **Hàm/Cú pháp**                     | **Chức năng**                                                     | **Ví dụ**                                                       |
| ----------------------------------- | ----------------------------------------------------------------- | --------------------------------------------------------------- |
| `keys()`                            | Trả về danh sách các key trong dictionary.                        | `list(my_dict.keys())` → `['a', 'b']`                           |
| `values()`                          | Trả về danh sách các value trong dictionary.                      | `list(my_dict.values())` → `[1, 2]`                             |
| `items()`                           | Trả về danh sách các tuple (key, value).                          | `list(my_dict.items())` → `[('a', 1), ('b', 2)]`                |
| `for key in my_dict`                | Lặp qua các key trong dictionary.                                 | `for key in my_dict: print(key)` → `a\nb`                       |
| `for key, value in my_dict.items()` | Lặp qua cả key và value.                                          | `for k, v in my_dict.items(): print(k, v)` → `a 1\nb 2`         |

  

---

  

## 5. Các ứng dụng đặc biệt

  

| **Cách sử dụng**         | **Mô tả**                                                                 | **Ví dụ**                                                       |
| ------------------------ | ------------------------------------------------------------------------- | --------------------------------------------------------------- |
| Dictionary Comprehension | Tạo dictionary từ một biểu thức hoặc vòng lặp.                            | `{x: x**2 for x in range(3)}` → `{0: 0, 1: 1, 2: 4}`            |
| Đảo ngược dictionary     | Đổi vị trí key và value.                                                  | `{v: k for k, v in my_dict.items()}`                            |
| Đếm tần suất xuất hiện   | Sử dụng dictionary để đếm tần suất các phần tử trong danh sách.           | `freq = {x: lst.count(x) for x in set(lst)}`                    |

  

---

  

# Tuple trong Python

  

## 1. Khởi tạo tuple

  

| **Cách khởi tạo**                         | **Mô tả**                                                                                   | **Ví dụ**                         |
| ----------------------------------------- | ------------------------------------------------------------------------------------------- | --------------------------------- |
| Sử dụng dấu ngoặc `()`                    | Khởi tạo tuple thông thường.                                                                | `my_tuple = (1, 2, 3)`            |
| Tuple rỗng                                | Tạo một tuple rỗng.                                                                         | `empty_tuple = ()`                |
| Tuple chứa một phần tử                    | Phải có dấu phẩy sau phần tử để phân biệt với kiểu dữ liệu khác.                            | `single_element = (1,)`           |
| Sử dụng `tuple()`                         | Tạo tuple từ iterable (list, string, set, v.v.).                                            | `my_tuple = tuple([1, 2, 3])`     |
| Tuple không có ngoặc                      | Python cho phép bỏ ngoặc khi khai báo các giá trị phân tách bằng dấu phẩy.                  | `my_tuple = 1, 2, 3`              |

  

---

  

## 2. Tính chất của tuple

  

1. **Không thể thay đổi (Immutable):** Một khi được khởi tạo, giá trị của tuple không thể thay đổi.

2. **Có thể chứa các kiểu dữ liệu khác nhau:** Tuple có thể chứa số, chuỗi, danh sách, hoặc thậm chí tuple khác.

  

---

  

## 3. Các thao tác cơ bản với tuple

  

| **Cú pháp/Phương thức**        | **Chức năng**                                                              | **Ví dụ**                               |
| ------------------------------ | -------------------------------------------------------------------------- | --------------------------------------- |
| `my_tuple[index]`              | Truy cập phần tử tại vị trí `index`.                                       | `(1, 2, 3)[0]` → `1`                    |
| `my_tuple[start:end:step]`     | Lấy một phần tử con (slicing).                                             | `(1, 2, 3, 4)[1:3]` → `(2, 3)`          |
| `len(my_tuple)`                | Trả về số lượng phần tử trong tuple.                                       | `len((1, 2, 3))` → `3`                  |
| `my_tuple.index(value)`        | Tìm vị trí đầu tiên của giá trị `value`.                                   | `(1, 2, 3).index(2)` → `1`              |
| `my_tuple.count(value)`        | Đếm số lần xuất hiện của giá trị `value`.                                  | `(1, 2, 2, 3).count(2)` → `2`           |
| `value in my_tuple`            | Kiểm tra xem `value` có trong tuple không.                                 | `2 in (1, 2, 3)` → `True`               |
| `value not in my_tuple`        | Kiểm tra xem `value` không có trong tuple.                                 | `4 not in (1, 2, 3)` → `True`           |

  

---

  

## 4. Các thao tác đặc biệt

  

| **Thao tác**                   | **Chức năng**                                                            | **Ví dụ**                               |
| ------------------------------ | ------------------------------------------------------------------------ | --------------------------------------- |
| Gán tuple (unpacking)          | Gán giá trị trong tuple vào các biến.                                    | `a, b, c = (1, 2, 3)` → `a=1, b=2, c=3` |
| Nối tuple                      | Kết hợp hai tuple.                                                       | `(1, 2) + (3, 4)` → `(1, 2, 3, 4)`      |
| Nhân tuple                     | Lặp lại tuple nhiều lần.                                                 | `(1, 2) * 3` → `(1, 2, 1, 2, 1, 2)`     |
| Lồng ghép tuple               | Tuple có thể chứa các tuple khác.                                        | `nested = (1, (2, 3), (4, (5, 6)))`    |

  

---

  

## 5. Các ứng dụng thực tế

  

- **Tuple thường dùng để lưu trữ dữ liệu không đổi** như tọa độ, cặp giá trị (`key, value`) hoặc cấu trúc bất biến.

- **Tuple làm khóa trong dictionary**: Vì tuple không thay đổi nên chúng có thể được sử dụng làm khóa trong dictionary.

  

---