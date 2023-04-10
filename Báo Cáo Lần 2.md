# Kĩ Thuật Giấu Tin Bằng Golden Ratio Base

## 1. Tổng Quan Về Golden ratio base

 Cơ số tỷ lệ vàng là một cơ số không nguyên sử dụng tỷ lệ vàng, được biểu thị bằng chữ cái Hy Lạp phi (φ), làm cơ sở của nó. Trong hệ thống này, mỗi chữ số là 0 hoặc 1 và mỗi vị trí đại diện cho một lũy thừa của tỷ lệ vàng.Chữ số "1" tương ứng với giá trị của một lũy thừa của phi. Cụ thể, giá trị của mỗi lũy thừa của phi được tính bằng cách nhân phi với chính nó.Chữ số "0" tương ứng với một số nguyên dương.
 
 Giá trị của tỷ lệ vàng xấp xỉ [(1 + √5)/2] ≈ 1,61803398875..., và nó thỏa mãn phương trình φ = 1 + 1/φ. Sử dụng thuộc tính này, chúng ta có thể biểu diễn bất kỳ số thực dương nào bằng cách sử dụng các chữ số 0 và 1 theo một cách duy nhất.
 
 Ví dụ, số 1 trong cơ sở tỷ lệ vàng được biểu diễn là 1φ, có nghĩa là 1 nhân với tỷ lệ vàng theo lũy thừa của 1 (nghĩa là 1φ = φ). Số 2 được biểu diễn bằng 10φ, có nghĩa là 1 lần tỷ lệ vàng với lũy thừa 1 cộng với 0 lần tỷ lệ vàng với lũy thừa 0 (tức là 10φ = φ + 0).

### Các ví dụ khác về số trong cơ sở tỷ lệ vàng bao gồm:



| Số Thập Phân | Lũy Thừa của φ | φ    |
| ------------ | -------------- | ---- |
|    1         |    φ 0        |  1    |
|    2         |    φ 1 + φ −2 |  10.01     |
|    3         |    φ 2 + φ −2            | 100.01      |
|    4          |   φ 2 + φ 0 + φ −2      | 101.01  |
|    5          |   φ 3 + φ −1 + φ −4         |   1000.1001|
|    6          |   φ 3 + φ 1 + φ −4      |  1010.0001    |
|    7          |   φ 4 + φ −4             | 10000.0001   |
|    8          |   φ 4 + φ 0 + φ −4         |10001.0001|
|    9          |   φ 4 + φ 1 + φ −2 + φ −4  |   10010.0101|
|    10          |  φ 4 + φ 2 + φ −2 + φ −4  | 10100.0101 |

 Cơ sở tỷ lệ vàng đã được nghiên cứu trong toán học và khoa học máy tính như một giải pháp thay thế tiềm năng cho ký hiệu nhị phân hoặc thập phân để biểu diễn các số. Tuy nhiên, nó đã không được sử dụng rộng rãi do sự phức tạp của nó và thiếu các ứng dụng thực tế.

## 2. Viết số cơ sở tỷ lệ vàng ở dạng tiêu chuẩn
 Trong ví dụ sau, ký hiệu 1 được sử dụng để biểu diễn −1.
 211.0 1 φ không phải là số cơ số φ tiêu chuẩn, vì nó chứa "11" và thêm "2" và " 1 " = −1, không phải là "0" hoặc "1".

 Để "chuẩn hóa" một số, chúng ta có thể sử dụng các phép thay thế sau: 011 φ = 100 φ , 0200 φ = 1001 φ , 0 1 0 φ = 1 01 φ và 1 1 0 φ = 001 φ . Chúng tôi có thể áp dụng các thay thế theo bất kỳ thứ tự nào chúng tôi muốn, vì kết quả là như nhau. Dưới đây, các thay thế được áp dụng cho số trên dòng trước nằm ở bên phải, số kết quả ở bên trái.

```
211.0 1 φ	
300,0 1 φ	011 φ → 100 φ
1101.0 1 φ	0200φ → 1001φ _
10001,0 1 φ	011 φ → 100 φ (lại)
10001. 1 01 φ	0 1 0 φ → 1 01 φ
10000,011 φ	1 1 0 φ → 001 φ
10000,1φ _	011 φ → 100 φ (lại)
```

 Bất kỳ số dương nào có biểu diễn cơ sở-φ kết thúc không theo tiêu chuẩn đều có thể được chuẩn hóa duy nhất theo cách này. Nếu chúng ta đạt đến điểm mà tất cả các chữ số là "0" hoặc "1", ngoại trừ chữ số đầu tiên là số âm , thì số đó sẽ là số âm. (Ngoại lệ cho trường hợp này là khi chữ số đầu tiên là một âm và hai chữ số tiếp theo là một, chẳng hạn như 1 111,001=1,001.) Điều này có thể được chuyển đổi thành âm của biểu diễn cơ số φ bằng cách phủ định mọi chữ số, chuẩn hóa kết quả, và sau đó đánh dấu nó là tiêu cực. Ví dụ: sử dụng dấu trừ hoặc một số ý nghĩa khác để biểu thị số âm. Nếu số học đang được thực hiện trên máy tính, một thông báo lỗicó thể được trả lại.

## 3. Mối quan hệ với mã hóa Fibonacci
 [Mã hóa Fibonacci](https://www.wikiwand.com/en/Fibonacci_coding) là một hệ thống số liên quan chặt chẽ được sử dụng cho các số nguyên. Trong hệ thống này, chỉ các chữ số 0 và 1 được sử dụng và giá trị vị trí của các chữ số là các số Fibonacci . Cũng như cơ số φ, dãy chữ số "11" có thể tránh được bằng cách sắp xếp lại thành dạng chuẩn, sử dụng quan hệ truy hồi Fibonacci Fk +1 = F k + F k −1 . Ví dụ: 

30 = 1×21 + 0×13 + 1×8 + 0×5 + 0×3 + 0×2 + 1×1 + 0×1 = 10100010

## 4. picoCTF 2023 UnforgottenBits Challenge

Những công đoạn trước mình đã làm phần [wu picoCTF 2023](https://hackmd.io/m9EzAVwCSNyqb31iX_6QLg?view) rồi . Phần này mình chỉ tập trung chủ yếu vào phần Giải Mã Golden Ratio Base. 

Đoạn mã Golden Ratio Base đã bị sai format :
```
01010010100.01001001000100.01001010000100.00101010010101.01000100100100.00100100000100.01000100000101.01000100001010.00000100000001.00001001010000.00000100010010.01000100010010.01001001001000.10001001000101.01001001010000.00001001000100.01001001010001.00000100000010.01000100010000.00001001001000.10000100010100.01000000010100.01001010000010.00101001010000.00001010101000.10000100100100.00101001000100.01000100010100.01001001010001.00000100010010.01000100010000.00001001000101.01000100010010.01000100010001.00000100001000.10001001000101.01001001001010.00000100010100.01000100000100.01000100010001.00000100000001.00000100001010.00000100010001.00001001000100.01000100000001.00000100001010.00000100001000.10000100000001.00000100010010.01001001001010.00000100000100.01000100010001.00000100001000.10001001010000.00001001010000.00000100000101.01001001000100.01000100010010.01000100010010.01001001000100.01000100010010.01000100000101.01001001000100.01001001001010.00000100010100.01000100010001.00000100000100.01000100000100.01000100000010.01000100010001.00001001000101.01000100010010.01000100000010.01001001010001.00001001001010.00001001001000.10000100000100.01001001000101.01001001000101.01000100010010.01001001010000.00000100010010.01001001001000.10001001000100.01000100010010.01000100010001.00000100000101.01000100010000.00001001001010.00001001000100.01000000010100.01001001010101.01001010100010.00100100100100.00100100010100.01000100000001.00000100010010.01000100001000.10000100001010.00000100010010.01001001010000.00000100001000.10000100010010.01001001010001.00001001001000.10000100010010.01001001001010.00001001000101.01000100000010.01001001001000.10000100001010.00001001000100.01000100001000.10000100010000.00001001010001.00000100000010.01000100010010.01001001010001.00000100000001.00001001010001.00001001010000.00001001000101.01000100000010.01000100000010.01000100010100.01001001010001.00000000010100.010
```
### Cách kiểm tra định dạng của Golden Ratio Base
```
Để kiểm tra đúng định dạng của số cơ sở tỷ lệ vàng, ta có thể sử dụng công thức sau để tính giá trị của nó:

số cơ sở tỷ lệ vàng = a_0 * phi^0 + a_1 * phi^1 + a_2 * phi^2 + ... + a_n * phi^n

Trong đó:

a_0, a_1, a_2, ..., a_n là các chữ số của số đó (0 hoặc 1)
phi là tỷ lệ vàng, có giá trị là khoảng 1.61803398875
Nếu chuỗi số có đúng định dạng của số cơ sở tỷ lệ vàng, thì kết quả tính toán của công thức trên sẽ là một số gần đúng với chuỗi đó. Nếu không, thì kết quả tính toán sẽ khác với chuỗi đó.

Ví dụ, để kiểm tra xem chuỗi số "101010" có phải là số cơ sở tỷ lệ vàng hay không, ta sử dụng công thức trên như sau:

số cơ sở tỷ lệ vàng = 1 * phi^0 + 0 * phi^1 + 1 * phi^2 + 0 * phi^3 + 1 * phi^4 + 0 * phi^5
= 1 + 0 + 2.61803398875 + 0 + 4.2360679775 + 0
= 7.85410196625

Kết quả tính toán của công thức trên không giống với chuỗi "101010", cho nên chuỗi này không phải là số cơ sở tỷ lệ vàng.
```

### Bắt đầu viết kịch bản cho nó : 

 `Ý tưởng : Để đúng với format nó thì đầu tiên mình lấy 15 chữ số nhị phân trong đống mã đó chuyển nó sang số phigital. Mã Phigital là một hệ thống số Phi cơ số trong đó các chữ số là 0 hoặc 1 và cơ số là tỷ lệ vàng Phi, xấp xỉ bằng 1,6180339887 , sau đó chuyển nó sang hệ thập phân (dec) và in ra kết quả là ACSII`.
```
import math

Phi=(math.sqrt(5)+1)/2 #((1 + √5)/2)

class PHIC:
	def __init__(self, p, c):
		self.phi = p
		self.one = c

	def toStr(self):
		if self.phi == 0:
			return self.one
		return str(self.phi) + "Phi" + ("+" if self.one > 0 else "") + (str(self.one) if self.one != 0 else "")

def fib(n):
    if n == 0:
        return 0
    elif n == 1:
        return 1
    elif n < 0:
        return (-1)**(-n+1)*fib(-n)
    else:
        return fib(n-1) + fib(n-2)

def addPHIC(p, q):
	return PHIC(p.phi + q.phi, p.one + q.one)

def phipowPHIC(p):
	return PHIC(fib(p), fib(p-1))

def phigitstodec(phigits):
	dp = phigits.find('.')
	DEC = PHIC(0,0)
	for i in range(len(phigits)):
		if phigits[i] == '1':
			pw = (dp - i - (1 if i < dp else 0))
			DEC = addPHIC(DEC, phipowPHIC(pw))

	# print(DEC.toStr())
	return DEC.phi*Phi+DEC.one

bits = '01010010100.01001001000100.01001010000100.00101010010101.01000100100100.00100100000100.01000100000101.01000100001010.00000100000001.00001001010000.00000100010010.01000100010010.01001001001000.10001001000101.01001001010000.00001001000100.01001001010001.00000100000010.01000100010000.00001001001000.10000100010100.01000000010100.01001010000010.00101001010000.00001010101000.10000100100100.00101001000100.01000100010100.01001001010001.00000100010010.01000100010000.00001001000101.01000100010010.01000100010001.00000100001000.10001001000101.01001001001010.00000100010100.01000100000100.01000100010001.00000100000001.00000100001010.00000100010001.00001001000100.01000100000001.00000100001010.00000100001000.10000100000001.00000100010010.01001001001010.00000100000100.01000100010001.00000100001000.10001001010000.00001001010000.00000100000101.01001001000100.01000100010010.01000100010010.01001001000100.01000100010010.01000100000101.01001001000100.01001001001010.00000100010100.01000100010001.00000100000100.01000100000100.01000100000010.01000100010001.00001001000101.01000100010010.01000100000010.01001001010001.00001001001010.00001001001000.10000100000100.01001001000101.01001001000101.01000100010010.01001001010000.00000100010010.01001001001000.10001001000100.01000100010010.01000100010001.00000100000101.01000100010000.00001001001010.00001001000100.01000000010100.01001001010101.01001010100010.00100100100100.00100100010100.01000100000001.00000100010010.01000100001000.10000100001010.00000100010010.01001001010000.00000100001000.10000100010010.01001001010001.00001001001000.10000100010010.01001001001010.00001001000101.01000100000010.01001001001000.10000100001010.00001001000100.01000100001000.10000100010000.00001001010001.00000100000010.01000100010010.01001001010001.00000100000001.00001001010001.00001001010000.00001001000101.01000100000010.01000100000010.01000100010100.01001001010001.00000000010100.010'
a = [bits[i:i+15] for i in range(0, len(bits), 15)]

res = []
for i in a:
	res.append(math.ceil(phigitstodec(i)))

print(bytes(res).decode())
```

* Giải Thích :
```
Mã xác định một số chức năng và một lớp:

math.sqrt(5)+1)/2tính giá trị của Phi.

class PHIC:định nghĩa một lớp đại diện cho một số phigital dưới dạng kết hợp của hai giá trị: phi và một. Phi đại diện cho hệ số của Phi trong số, trong khi một đại diện cho hệ số của giá trị đơn vị (1) trong số.

def fib(n):định nghĩa một hàm đệ quy để tính số Fibonacci thứ n.

def addPHIC(p, q):định nghĩa một chức năng để thêm hai số phigital.

def phipowPHIC(p):định nghĩa một hàm để tính lũy thừa thứ p của Phi dưới dạng một số phigital.

def phigitstodec(phigits):định nghĩa một hàm để chuyển đổi một số phigital được biểu thị dưới dạng một chuỗi các số 0 và 1 thành số thập phân tương đương của nó dưới dạng một số phigital.

bits = '...'xác định thông điệp nhị phân trong mã phigital.

a = [bits[i:i+15] for i in range(0, len(bits), 15)]chia thông điệp nhị phân thành các nhóm 15 bit.

res = []khởi tạo một danh sách trống để lưu trữ số thập phân tương đương của mỗi số phigital.

for i in a:lặp qua từng nhóm 15 bit.

res.append(math.ceil(phigitstodec(i)))chuyển đổi số phigital được biểu thị bằng 15 bit thành số thập phân tương đương, làm tròn thành số nguyên gần nhất và nối kết quả vào danh ressách.

print(bytes(res).decode())chuyển đổi danh sách các giá trị thập phân thành các ký tự ASCII và in thông báo kết quả.
```

=> chạy kịch bản và mình nhận được key, salt và iv mới 

![](https://i.imgur.com/DzbaaV1.png)


Refs : 

https://en.wikipedia.org/wiki/Golden_ratio_base
https://math.stackexchange.com/questions/3413457/what-does-the-golden-ratio-look-like-in-other-base-systems
https://dbpedia.org/page/Golden_ratio_base


 