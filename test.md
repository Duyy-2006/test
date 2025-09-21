# BUỔI 2: TOÁN TỬ LOGIC, CẤU TRÚC RẼ NHÁNH
``` Update thêm
- Code mẫu của toán tử ba ngôi
- Cho ví dụ để thấy tầm quan trọng của break trong switch case
```
- [BUỔI 2: TOÁN TỬ LOGIC, CẤU TRÚC RẼ NHÁNH](#buổi-2-toán-tử-logic-cấu-trúc-rẽ-nhánh)
  - [A. Mục tiêu kiến thức:](#a-mục-tiêu-kiến-thức)
  - [B. Phương pháp:](#b-phương-pháp)
  - [C. Chuẩn bị:](#c-chuẩn-bị)
  - [D. Tiến trình bài giảng:](#d-tiến-trình-bài-giảng)
    - [1. Toán tử logic, quan hệ trong C:](#1-toán-tử-logic-quan-hệ-trong-c)
      - [a. Toán tử quan hệ:](#a-toán-tử-quan-hệ)
      - [b. Toán tử logic:](#b-toán-tử-logic)
        - [Note:](#note)
    - [2.  Cấu trúc câu lệnh rẽ nhánh:](#2--cấu-trúc-câu-lệnh-rẽ-nhánh)
      - [a. Câu lệnh if...else](#a-câu-lệnh-ifelse)
        - [Ví dụ thực tiễn:](#ví-dụ-thực-tiễn)
      - [b. Switch case trong C:](#b-switch-case-trong-c)
    - [3. Bài tập](#3-bài-tập)
    - [Bonus: Toán tử 3 ngôi](#bonus-toán-tử-3-ngôi)




## A. Mục tiêu kiến thức:
1. Nắm vững được cách sử dụng các toán tử logic, dùng câu lệnh if…else để rẽ nhánh
2. Hoàn thành các bài tập cơ bản trên Codeforces




## B. Phương pháp:
 1. Đặt vấn đề.
 2. Triển khai các nội dung.
 3. Thực hành trên Dev-C++, VSCode...
## C. Chuẩn bị:
1. Người dạy: Laptop, file giáo án.
2. Người học: Laptop, tìm hiểu trước về nội dung bài học.


## D. Tiến trình bài giảng:
### 1. Toán tử logic, quan hệ trong C:
#### a. Toán tử quan hệ:
- Định nghĩa: Toán tử quan hệ dùng để kiểm tra mối quan hệ giữa hai toán hạng. Trả về giá trị **đúng(1) hoặc sai(0)**.
- Bảng dưới đây chỉ ra tất cả các toán tử quan hệ được hỗ trợ bởi ngôn ngữ C. Giả sử rằng biến A có giá trị 10 và biến B có giá trị 20, ta có:


| Toán tử  |Miêu tả   |Ví dụ   |
|---|---|---|
|==   | Kiểm tra nếu 2 toán hạng bằng nhau hay không. Nếu bằng thì trả về 1.  | (A == B) là không đúng.=> (A==B) = 0   |
|  != | Kiểm tra 2 toán hạng có giá trị khác nhau hay không. Nếu không bằng thì trả về 1.  |(A != B) là đúng.=> ( A==B ) = 1|
|  > |Kiểm tra nếu toán hạng bên trái có giá trị lớn hơn toán hạng bên phải hay không. Nếu lớn hơn thì trả về 1.   | (A > B) là không đúng => ( A > B) = 0  |
|  < | Kiểm tra nếu toán hạng bên trái nhỏ hơn toán hạng bên phải hay không. Nếu nhỏ hơn thì trả về 1.  | (A < B) là đúng.=> ( A < B ) = 1  |
|  >= |Kiểm tra nếu toán hạng bên trái có giá trị lớn hơn hoặc bằng giá trị của toán hạng bên phải hay không. Nếu đúng trả về 1.   |(A >= B) là không đúng.=> ( A >= B) = 0   |
|  <= |Kiểm tra nếu toán hạng bên trái có giá trị nhỏ hơn hoặc bằng toán hạng bên phải hay không. Nếu đúng trả về 1.   |(A <= B) là đúng.=> ( A <= B ) = 1   |




#### b. Toán tử logic:
- Định nghĩa: Có 3 toán tử logic là AND (&&) , OR (||) , NOT (!), các toán tử logic này được sử dụng để kết hợp nhiều toán hạng (biểu thức so sánh hoặc giá trị đúng sai) và sẽ trả về đúng(1) hoặc sai(0).
##### Note:
Trong C thì tất cả các giá trị khác 0 được coi là giá trị đúng.
giả sử toán hạng thứ 1 là biến A, toán hạng thứ 2 là biến B, toán hạng thứ 3 là biến C.
- A, B, C có thể là 1 số, 1 toán tử so sánh, 1 biểu thức …
- Người dạy đưa một số ví dụ.
- Bảng dưới đây chỉ rõ tất cả các toán tử logic được hỗ trợ bởi ngôn ngữ C. **A có giá trị  = 1, B có giá trị = 0, C có giá trị = 0.**


|Toán tử   |Ý nghĩa   |Cách hoạt động   |Ví dụ   |
|---|---|---|---|
| &&  |Toán tử AND(Và)   |Cho giá trị đúng khi mọi toán hạng có giá trị đúng, sai trong các trường hợp còn lại   |(A && B) = 0 Vì A đúng, B sai Cụ thể:( 2 < 3 && 3 > 5) = 0;( 3 % 3 == 0 && 1 < 2) = 1   |
|  II    |Toán tử OR(Hoặc)   |Cho giá trị sai khi mọi toán hạng có giá trị sai, đúng trong các trường hợp còn lại   |(A || B) = 1 Vì A, B không cùng sai;(B || C) = 0. Vì B, C cùng sai   |
|  ! |Toán tử NOT(phủ định)   |Phủ định của đúng là sai, phủ định của sai là đúng   |!(A) = 0. Vì A đúng !( A && B) = 1. Vì ( A && B) = 0   |
+ viết bảng chân lý để giải thích (0 là sai, 1 là đúng)


### 2.  Cấu trúc câu lệnh rẽ nhánh:
#### a. Câu lệnh if...else
- Chú ý lấy ví dụ thực tế nhiều, ví dụ: Hôm nay nếu trời mưa thì…
(giải thích bằng sơ đồ khối)
- Mệnh đề if else trong C được sử dụng để kiểm tra xem một biểu thức đk nào đó có đúng hay không, nếu đúng thì thực hiện những câu lệnh bên trong khối lệnh if , nếu sai thì bỏ qua những câu lệnh đó và thực hiện câu lệnh trong khối lệnh else nếu có.
- Người dạy chính có thể dùng sơ đồ khối để các em hiểu về “rẽ nhánh”
- Mệnh đề if trong C:
```cpp
if (condition) {
  // khối lệnh này được thực thi nếu condition = true
}
```
![markdown](anh1.png)


- Mệnh đề if-else trong C:
If có thể không cần đến else nhưng else thì cần if đi trước.
```cpp
if (condition) {
  // khối lệnh này được thực thi nếu condition = true
} else {
  // khối lệnh này được thực thi nếu condition = false
}
```
![markdown](anh2.png)


- Chú ý : Trong C các giá trị khác 0 được coi là đúng nếu bạn có thể sử dụng nó để làm điều kiện cho if.
- Nếu số mà bạn truyền vào làm điều kiện cho if khác 0 thì code trong if sẽ thực thi và ngược lại.
- Lấy ví dụ về if- else với điều kiện được truyền vào là 1 số.
- VD:
  + Làm bài tập về chẵn lẻ
   
- Mệnh đề if-elseif-else trong C:
 ```cpp
if (condition1) {
  // khối lệnh này được thực thi nếu condition1 = true
} else if (condition2) {
  // khối lệnh này được thực thi nếu condition1 = false và condition2 = true
...
} else {
  // khối lệnh này được thực thi nếu nếu tất cả những điều kiện trên = false
}
```
![markdown](anh3.png)
##### Ví dụ thực tiễn:
 Từ nhà em đến trường có 3 con đường a, b, c,  con đường a có quán bánh mì, con đường b có quán cơm, con đường c có quán nước. Nếu trên đường đi học em ăn bánh mì thì em đi con đường a, nếu em ăn cơm thì em đi đường b, nếu em uống nước thì em đi đường c.
=> Đưa ra câu hỏi?
- Tại sao phải dùng if - else if - else thay vì 1 loạt các lệnh if?
- Đó là vì cấu trúc else if sẽ gắn các lệnh này thành 1 khối thay vì tách rời như 1 loạt các lệnh if. Điều này giúp chương trình thực hiện nhanh hơn, nếu điều kiện đúng ở đâu thì nó sẽ dừng ở đó và không xét các điều kiện sau đấy nữa. Còn đối với 1 loạt các lệnh if thì chương trình phải kiểm tra tất cả
VD:
- Nhập vào tên một người, nếu tên là “A” thì in ra là “Bố”, “B” thì in ra là “Mẹ”, còn không thì in ra không biết
- Mệnh đề if-else lồng nhau:
    - If else có thể lồng vào nhau tức là bên trong khối if else cũng có thể có thêm nhiều câu lệnh if else khác.
    - Thông thường if else lồng nhau được sử dụng khi điều kiện của bài toán của bạn quá lớn và cần chia nhỏ ra làm nhiều phần để kiểm tra từng bước một.
```cpp
if (condition A) {
  // khối lệnh này được thực thi nếu condition A = true
 if (condition1) {
    // khối lệnh này được thực thi nếu condition1 = true
…
} else {
   // khối lệnh này được thực thi nếu condition 1 = false
}
} else{
// khối lệnh này được thực thi nếu nếu condition A = false




   if (condition 2) {
    // khối lệnh này được thực thi nếu condition2 = true
…
} else {
   // khối lệnh này được thực thi nếu condition 2 = false
}
}
```
- Người dạy có thể lấy  Ví dụ  : Kiểm tra n nằm trong đoạn [20, 50] và chia hết cho ít nhất 1 trong 4 số 2, 3, 5, 7, nếu đúng in YES, ngược lại in NO
 
#### b. Switch case trong C:
- Lệnh switch case là một cấu trúc rẽ nhánh hoàn toàn có thể thay thế bằng cấu trúc if-else.
- Tuy nhiên trong một số trường hợp, việc dùng switch case sẽ giúp code chúng ta dễ viết và dễ đọc hơn, tối ưu hơn.
Cú pháp:
```cpp
switch(value){
case c1:
 //code
 break;
case c2:
 //code
 break;
.... case n:
 //code
break;
default:
 //code
}
```
Trong đó :
- Expression là giá trị hằng số và được so sánh với các giá trị của các case.
- Nếu có một case nào đó khớp giá trị thì ta thực hiện khối lệnh tương ứng với case đó cho tới khi gặp lệnh “break”;
- Giới thiệu về break và nói về tầm quan trọng của break trong switch case (có thể lấy một ví dụ không có break để cho các em dễ hiểu).


VD: Tầm quan trọng của break (Code này không có break và khi nhập n = 2 sẽ in ra toàn bộ từ case 2 trở xuống):
```cpp
switch (n) {
        case 1:
            cout << "Ban chon so 1\n";
        case 2:
            cout << "Ban chon so 2\n";
        case 3:
            cout << "Ban chon so 3\n";
        default:
            cout << "Khong hop le\n";
    }
```








- Case default sẽ được thực hiện nếu không có case nào khớp với giá trị Expression.
Sơ đồ khối :
 
VD:
- Nhập vào 1 số, in ra tên thứ đó trong tuần (tiếng anh)
- Nhập vào 1 số, in ra số ngày trong tháng (tháng 2 mặc định là 28 ngày)


### 3. Bài tập      
- Kiểm tra tính chẵn lẻ của một số
- Tìm max trong 3 số
- Ở đây có thể giới thiệu về toán tử 3 ngôi và yêu cầu các em làm lại bài kiểm tra chẵn lẻ với yêu cầu dung toán tử 3 ngôi.
 
### Bonus: Toán tử 3 ngôi
Cú pháp: Biểu thức logic ? nếu đúng trả về : nếu sai trả về
(giá trị trả về ở cả 2 vế phải cùng kiểu)
``` cpp
int main(){
  //Định nghĩa biến
  int a = 2, b = 3;
  // Tìm số lớn nhất
  int max = (n1 > n2) ? n1:n2;
  //Giải nghĩa: Nếu n1 > n2 thì max = n1 không thì max = n2
  //In ra số lớn nhất
  printf("So lon nhat la %d", max);
}
```
- Cho các em thêm 1 2 bài nữa để quen với cấu trúc rồi giới thiệu với các em về thư viện math.h và một số hàm hay dung trong thư viện (sqrt, abs, fabs)
abs giá trị tuyệt đối cho số nguyên, fabs giá trị tuyệt đối cho số thực (thường thì dùng abs cho cả số thực và nguyên đều được)
 
- Cho các em làm bài kiểm tra số chính phương để tận dụng được cả 2 kiến thức vừa học.



