---
layout: document
title: Code PEP8
---

# Quy chuẩn code trong Python

PEP8 là một quy chuẩn mã nguồn cho Python, nhằm mục đích cải thiện khả năng đọc và tính nhất quán của mã nguồn. Điều này hạn chế việc không có tính thống nhất trong việc lập trình các dự án.

## 1. Số lượng ký tự trên 1 dòng
- Tối đa 79 ký tự
- Đối với các khối code hạn chế về cấu độ dài giới hạn ở 72 ký tự

**Đúng**


```python
def long_function_name(var_one, var_two, var_three, var_four):
    print(var_one)
```

**Sai**


```python
def long_function_name(var_one, var_two, var_three, var_four, var_five, var_six, var_seven): # 92 characters
    print(var_one)
```

## 2. Sử dụng thụt lề
- Sử dụng 4 dấu cách cho mỗi cấp độ thụt lề
- Không nên sử dụng dấu tab


```python
def hello_world():
    print("Hello World")
```


```python
foo = long_function_name(var_one, var_two,
                         var_three, var_four)
```

## 3. Cách đặt tên

- **Biến và hàm:** Sử dụng chữ thường nối cụm từ bằng dấu `_`

- Để phân biệt tránh nhầm lẫn cả hai: biến thường đặt theo danh từ trong khi đó hàm sẽ được đặt là động từ


```python
my_variable = 10

def my_function():
    pass
```

- **Lớp**: Sử dụng chữ cái in hoa ở mỗi từ đầu tiên


```python
class MyClass:
    pass
```

- **Hằng số:** Sử dụng toàn bộ chữ in hoa nối các cụm từ bằng dấu `_`


```python
MAX_LIMIT = 100
```

## 4. Dòng trắng
- Sử dụng dòng trắng để tách biệt các lớp, hàm, và các khối mã lớn.
- Sử dụng hai dòng trắng trước định nghĩa của lớp hoặc hàm cấp cao.
- Sử dụng một dòng trắng giữa các phương thức trong một lớp.


```python
class MyClass:
    
    def method_one(self):
        pass

    def method_two(self):
        pass
```

## 5. Thêm thư viện/package

- Thêm thư viện/package được đặt ở đầu file
- Thứ tự nhập thư viện được chia ra cụ thể thành ba cụm:

    + Thư viện chuẩn
    + Thư viện bên thứ ba
    + Thư viện cục bộ



```python
import os
import sys

import pandas as pd

from mymodule import myfunction
```

## 6. Khoảng trắng trong biểu thức và câu lệnh

- Không sử dụng khoảng trắng dư thừa trong các biểu thức và câu lệnh.

**Đúng**


```python
a = b + c
```

**Sai**


```python
a = b+c
```

- Không sử dụng khoảng trắng xung quanh dấu bằng khi sử dụng cho đối số.

**Đúng**


```python
def my_function(param1, param2=2):
    pass
```

**Sai**


```python
def my_function(param1, param2 = 2):
    pass
```

- Mức độ ưu tiên toán tử khác nhau cần lưu ý đến khoảng trắng


```python
hypot2 = x*x + y*y
```

## 7. Comment

- Sử dụng nhận xét để giải thích các phần mã phức tạp.
- Nhận xét phải rõ ràng, ngắn gọn và phù hợp.


```python
# Đây là nhận xét
x = x + 1  # Tăng giá trị của x lên 1
```

## 8. Docstrings

- Sử dụng docstrings để mô tả các lớp và hàm.
- 3 dấu ngoặc kép (""") cho docstrings.


```python
def my_function():
    """
    Đây là chuỗi tài liệu của hàm.
    Hàm này không làm gì cả.
    """
    pass
```

## 9. Dấu ngoặc đơn 
Tránh sử dụng dấu ngoặc đơn không cần thiết.

**Hợp lý**


```python
x = (1+2) * (3+4)
```

**Chưa hợp lý**


```python
x = (( 1 + 2 ) * ( 3 + 4 ))
```

## 10. Xử lý khi dòng quá dài
Khi một dòng quá dài, sử dụng dấu gạch dưới `\` hoặc dấu ngoặc đơn để tiếp tục dòng.


```python
x = 1 + 2 + 3 + 4 + \
    5 + 6 + 7 + 8
```

Hoặc sử dụng dấu ngoặc ()


```python
x = (1 + 2 + 3 + 4
    + 5 + 6 + 7 + 8)
```

## 11. Biểu thức điều kiện

- Khi câu lệnh điều kiện quá dài ta nên tách dòng để dễ nhìn hơn


```python
if (condition1 and
    condition2 and
    condition3):
    do_something()
```

- Nên sử dụng toán tử `is not` thay vì `not ... is`
- Khi so sánh với `None` ta nên dùng `is` hoặc `is not`

## 12. Một số lưu ý khác

- Tránh gán nhiều giá trị trong cùng một dòng với nhau 


```python
x = 1
y = "a"
z = [3]

# Sai
x, y, z = 1, "a", [3]
```

## Nguồn tham khảo: 
- [PEP8](https://peps.python.org/pep-0008/)
