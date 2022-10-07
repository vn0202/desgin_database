# Cơ sở dữ liệu

 **Đề bài**: Tìm hiểu về CSDL 
 
 **Nguời thực hiện** : Vũ Văn Nghĩa. 
## DBMS

- DBMS là viết tắt của Database Management System( Hệ quản trị Cơ sở dữ liệu).
- Hệ quản trị cơ sở dữ liệu là phần mềm được thiết kế để có thể xác định, tiến hành các thao tác, truy xuất và quản lý
  dữ liệu trong CSDL.
- DBMS thường có khả năng tự thao tác với dữ liệu, định dạng dữ liệu, tên trường, cấu trúc bản ghi và cấu trúc tệp. Nó
  cũng xác định các quy tắc để xác nhận và thao tác với dữ liệu.
- Với DBMS, người dùng có thể thao tác sửa/xóa/thêm dữ liệu mà không còn cần các chương trình khung. Các ngôn ngữ lập
  trình truy vấn như SQL thường đi kèm với DBMS để lập trình viên dễ dàng tương tác với dữ liệu họ cần.
- Một vài DBMS nổi tiếng:

    - MySQL
    - SQL server
    - Oracle
    - dBASE

### RDBMS

- RDBMS viêt tắt của Relational Database Management System ( Hệ quản trị Cơ sở dữ liệu quan hệ ).
- Dữ liệu được tổ chức dưới dạng các bảng độc lập có tính logic. Mối quan hệ giữa
  các bảng được thể hiện thông qua dữ liệu được chia sẻ. Dữ liệu trong một bảng có thể tham chiếu dữ liệu trong các bảng
  khác, duy trì tính toàn vẹn của các liên kết giữa chúng.
  Tính năng này được gọi là tính toàn vẹn tham chiếu, một khái niệm quan trọng trong cơ sở dữ liệu quan hệ. Các hành
  động như "select" và "join" có thể được thực hiện trên các bảng dữ liệu.
  Đây là kiểu tổ chức cơ sở dữ liệu đang được sử dụng rộng rãi nhất.

### SQL

- Viết tắt của cụm từ Structured Query Language - Ngôn ngữ truy vấn cấu trúc là ngôn ngữ tiêu chuẩn mà bất kỳ
  hệ quản trị cơ sở dữ liệu quan hệ nào cũng phải đáp ứng.
- Một cách đơn giản, SQL là ngôn ngữ để bạn thao tác với CSDL.
- Các câu lệnh SQL được sử dụng để thực hiện các thao tác như chèn, cập nhật, xóa hay truy xuất dữ liệu từ CSDL.
- Các lệnh SQL tiêu chuẩn để tương tác với cơ sở dữ liệu quan hệ là CREATE, SELECT, INSERT, UPDATE, DELETE và DROP. Các
  lệnh này có thể được phân thành các nhóm sau dựa trên bản chất của chúng

### MySQL

- MySQL là 1 hệ thống quản trị về cơ sở dữ liệu với mã nguồn mở (được gọi tắt là RDBMS) và đang hoạt động theo mô hình
  dạng client-server.
- MySQL cho phép dữ liệu được lưu trữ và truy cập trên nhiều công cụ lưu trữ, bao gồm InnoDB, CSV và NDB. MySQL cũng có
  khả năng sao chép dữ liệu và phân vùng bảng để có hiệu suất và độ bền tốt hơn. Người dùng MySQL không bắt buộc phải
  học các lệnh mới; họ có thể truy cập dữ liệu của mình bằng các lệnh SQL tiêu chuẩn.

#### Kiểu dữ liệu trong Mysql
- Kiểu dữ liệu chuỗi 
<table>
<tbody>
  <tr>
    <th>Kiểu dữ liệu </th>
    <th>Mô tả </th>
  </tr>
  <tr>
    <td>CHAR(size)</td>
    <td>Một chuỗi độ dài CỐ ĐỊNH (có thể chứa các chữ cái, số và các ký tự đặc biệt). Tham số size chỉ định độ dài cột theo ký tự - có thể từ 0 đến 255. Mặc định là 1
    </td>
  </tr>
  <tr>
    <td>VARCHAR(size)</td> 
    <td>Một chuỗi độ dài BIẾN ĐỔI (có thể chứa các chữ cái, số và các ký tự đặc biệt). Tham số size chỉ định độ dài cột tối đa tính bằng ký tự - có thể từ 0 đến 65.535
    </td>
  </tr>
   <tr>
    <td>BINARY(size)	
    </td> 
    <td>Bằng CHAR (), nhưng lưu trữ các chuỗi byte nhị phân. Tham số size chỉ định độ dài cột tính bằng byte. Mặc định là 1</td>
  </tr>
   <tr>
    <td>TINYTEXT</td> 
    <td>Giữ một chuỗi có độ dài tối đa là 255 ký tự
    </td>
  </tr>
    <tr>
    <td>TEXT(size)	
    </td> 
    <td>Giữ một chuỗi có độ dài tối đa là 65.535 byte
    </td>
  </tr>
   <tr>
    <td>MEDIUMTEXT</td> 
    <td>Giữ một chuỗi có độ dài tối đa là 16.777.215 ký tự
    </td>
  </tr>
   <tr>
    <td>ENUM(val1, val2, val3, ...)	
    </td> 
    <td>Một đối tượng chuỗi chỉ có thể có một giá trị, được chọn từ danh sách các giá trị có thể có. Bạn có thể liệt kê tới 65.535 giá trị trong danh sách ENUM. Nếu một giá trị được chèn mà không có trong danh sách, một giá trị trống sẽ được chèn. Các giá trị được sắp xếp theo thứ tự nhập vào
    </td>
  </tr>
  <tr>
    <td>SET(val1, val2, val3, ...)	
    </td> 
    <td>Một đối tượng chuỗi có thể có 0 hoặc nhiều giá trị, được chọn từ danh sách các giá trị có thể có. Bạn có thể liệt kê tối đa 64 giá trị trong danh sách SET
    </td>
  </tr>
 

</tbody>
</table>

- Kiểu dữ liệu số : 


<table> 
  <tr>
    <th>Kiểu dữ liệu</th>
    <th> Mô tả </th>
  </tr>
  <tr>  
    <td>TINYINT(size)	
    </td>
    <td>Một số nguyên rất nhỏ. Phạm vi thông thường là từ -128 đến 127. Phạm vi Unsigned(*) là từ 0 đến 255. Tham số size chỉ định chiều rộng hiển thị tối đa (là 255)
    </td>
  </tr>
  <tr>  
    <td>BOOL</td>
    <td>Giá trị 0 được coi là sai, các giá trị khác 0 được coi là đúng.
    </td>
  </tr>
   <tr>  
    <td>BOOLEAN</td>
    <td>Tương tự Bool</td>
   </tr>
    <tr>  
    <td>SMALLINT(size)	
    </td>
    <td>Một số nguyên nhỏ. Phạm vi thông thường là từ -32.768 đến 32.767. Phạm vi Unsigned là từ 0 đến 65.535. Tham số size chỉ định chiều rộng hiển thị tối đa (là 255)
    </td>
   </tr>
    <tr>  
    <td>INT(size)	
    </td>
    <td>Một số nguyên trung bình. Phạm vi thông thường là từ -2.147.483.648 đến 2.147.483.647.  Phạm vi Unsigned là từ 0 đến 4.294.967.295. Tham số size chỉ định chiều rộng hiển thị tối đa (là 255)
    </td>
   </tr>
   <tr>  
    <td>FLOAT(p)	
    </td>
    <td>Một số có dấu thập phân động . MySQL sử dụng giá trị p để xác định xem nên sử dụng FLOAT hay DOUBLE cho kiểu dữ liệu kết quả. Nếu p từ 0 đến 24, kiểu dữ liệu sẽ trở thành FLOAT (). Nếu p từ 25 đến 53, kiểu dữ liệu trở thành DOUBLE ()
    </td>
   </tr>
   <tr>  
    <td>DOUBLE(size, d)	
    </td>
    <td>Một số bình thường có dấu thập phân không cố định. Tổng số chữ số được chỉ định trong tham số size. Số chữ số sau dấu thập phân được chỉ định trong tham số d
    </td>
   </tr>
   <tr>  
    <td>DECIMAL(size, d)	
    </td>
    <td>Một số có dấu thập phân chính xác. Tổng số chữ số được chỉ định trong tham số size. Số chữ số sau dấu thập phân được chỉ định trong tham số d. Số tối đa cho size là 65. Số lớn nhất cho d là 30. Giá trị mặc định cho size là 10. Giá trị mặc định cho d là 0.
    </td>
   </tr>
  
 
</table>

- Kiểu dữ liệu định dạng ngày, giờ: 


<table> 
  <tr>
    <th>Kiểu dữ liệu</th>
    <th> Mô tả </th>
  </tr>
  <tr>  
    <td>DATE	
    </td>
    <td>Định dạng kiểu ngày tháng: YYYY-MM-DD. Phạm vi được hỗ trợ là từ '1000-01-01' đến '9999-12-31'
    </td>
  </tr>
  <tr>  
    <td>DATETIME(fsp)	
    </td>
    Định dạng ngày và giờ kết hợp: YYYY-MM-DD hh:mm:ss. Phạm vi được hỗ trợ là từ '1000-01-01 00:00:00' đến '9999-12-31 23:59:59'. Thêm DEFAULT và ON UPDATE trong định nghĩa cột để tự động khởi tạo và cập nhật cho ngày và giờ hiện tại
    </td>
  </tr>
  <tr>  
    <td>TIMESTAMP(fsp)	
    </td>
    <td>Định dạng dấu thời gian. Giá trị TIMESTAMP được lưu trữ dưới dạng số giây kể từ giai đoạn Unix ('1970-01-01 00:00:00' UTC). Định dạng hiển thị sẽ là YYYY-MM-DD hh:mm:ss. Phạm vi được hỗ trợ từ '1970-01-01 00:00:01' UTC đến '2038-01-09 03:14:07' UTC. Có thể chỉ định tự động khởi tạo và cập nhật cho ngày và giờ hiện tại bằng cách sử dụng DEFAULT CURRENT_TIMESTAMP và ON UPDATE CURRENT_TIMESTAMP trong định nghĩa cột
    </td>
  </tr> 
  <tr>  
    <td>TIME(fsp)	
    </td>
    <td>Định dạng thời gian dưới dạng: hh:mm:ss. Phạm vi được hỗ trợ là từ '-838: 59: 59' đến '838: 59: 59'
    </td>
  </tr> 
  <tr>  
    <td> YEAR</td>
    <td>Định dạng năm dưới dạng bốn chữ số. Các giá trị được phép ở định dạng bốn chữ số là từ 1901 đến 2155 và 0000. MySQL 8.0 không hỗ trợ năm ở định dạng hai chữ số.
   </td>
  </tr>
</table>

 
 
#### SQL constraints

- các hạn chế SQL được sử dụng để chỉ rõ các quy tắc cho dữ liệu trong bảng 

-  các hạn chế được sử dụng để giới hạn kiểu dữ liệu cái mà có thể truyền vào 1 bảng. Điều này đảm bảo độ chính xác và tin cậy của dữ liệu trong bảng. Nếu có bất kỳ xung đột nào giữa các hạn chế và hoạt động dữ liệu, hoạt động sẽ bị bỏ qua. 

- các hạn chế có mức độ `table ` và `column`


  <table>
    <tr>
      <th>Tên </th>
      <th>Mô tả </th>
    </tr>
    <tr>
      <td>NOT NULL
      </td>
      <td> Đảm bảo rằng các cột không có giá trị null</td>
    </tr>
    <tr>
      <td>UNIQUE
      </td>
      <td>Đảm bảo tất cả các giá trị trong cột là khác nhau.
      </td>
    </tr>
    <tr>
      <td>PRIMARY KEY </td>
      <td>Sự kết hợp của NOT NULL và UNIQUE. Định danh duy nhất cho từng bản ghi của bảng.
  Trên một cái bảng chỉ được phép tồn tại tối đa một ràng buộc PRIMARY KEY.
</td>
    </tr>
    <tr>
      <td>FOREGIN KEY </td>
      <td>Ngăn cản các hành động có thể phá vỡ liên kết giữa các bảng. Khóa ngoại có thể được áp dụng cho 1 
hoặc nhiều cột và được sử dụng để liên kết hai bảng với nhau trong CSDL quan hệ.
    </td>CHECK </td>
    <td> Đảm bảo rằng giá trị trong cột thỏa mãn điều kiện nào đó. </td>
    </tr>
    <tr>
      <td>DEFAULTS</td>
      <td>Thiết lập giá trị mặc định cho cột nếu gíá trị không được chỉ rõ </td>
    </tr>
    <tr>
      <td> CREATE INDEX</td>
      <td> Đưọc sử dụng để tạo và nhận dữ liệu từ database nhanh chóng </td>
    </tr>
  </table>

#### Mối quan hệ 
Mối quan hệ (Relationship): tạo ra mối liên kết giữa hai bảng nhằm xác định mối liên quan giữa các trường dữ liệu của hai bảng.  Trong cơ sở dữ liệu quan hệ mối quan hệ thể hiện ở 03 dạng sau:
 
- Quan hệ 1 - 1 là 1 dòng (record) của bảng này liên kết với 1 dòng (record) duy nhất của bảng khác.
- Quan hệ 1 - nhiều - một dòng (record) của bảng một liên kết với nhiều dòng của bảng nhiều. Nói ngược lại thì nhiều dòng của bảng nhiều liên kết với một dòng ở bảng một
- Quan hệ n-n: trong quan hệ này một bảng ghi trong bảng này tương ứng với nhiều bảng ghi trong bảng kia và ngược lại.


#### Arrgregate functions 

1. Hàm COUNT(column_name)( Giá trị null không tính )

- Hàm trả về số lượng bản ghi khớp với điều kiện 

  ```sql
     SELECT COUNT(column_name)
     FROM table_name
      WHERE condition;
  ```
2. Hàm AVG(column)( Giá trị null bị bỏ qua)
  Hàm trả về giá trị trung bình của tập các bản ghi 

  ```sql
     SELECT AVG(Price)
      FROM Products;
  ```
3. Hàm SUM(column_name) ( Giá trị null bị bỏ qua)

 Hàm trả về giá trị tổng 
 
 ```sql 
 SELECT SUM(Quantity)
 FROM OrderDetails;
 ```
4. Hàm MIN()

 Hàm trả về giá trị nhỏ nhất trong tập bản ghi
 
```sql 
  SELECT MIN(column_name)
  FROM table_name
  WHERE condition;
```
5. Hàm MAX(column_name)
 
 Hàm trả về bản ghi có giá trị lớn nhất trong cột được chọn 
 
 ```sql
 SELECT MAX(column_name)
 FROM table_name
 WHERE condition;
 ```

#### Subquery 

- Sub query trong SQL hoặc truy vấn nội bộ hoặc truy vấn Nested là truy vấn trong một truy vấn SQL khác và được nhúng trong mệnh đề WHERE.
- Một sub query được sử dụng để trả về dữ liệu sẽ được sử dụng trong truy vấn chính như một điều kiện để hạn chế hơn nữa dữ liệu được truy xuất.
- Sub query có thể được sử dụng với câu lệnh SELECT, INSERT, UPDATE, và DELETE cùng với các toán tử như: =, <,>,> =, <=, IN, BETWEEN, v.v ...
- Có một vài quy tắc mà Sub query phải tuân theo: 
   
   - Sub query phải được đặt trong dấu ngoặc đơn.
   - Một sub query có thể chỉ có một cột trong mệnh đề SELECT, trừ khi nhiều cột trong truy vấn chính cho sub query để so sánh các cột đã chọn của nó.
   - Không thể sử dụng lệnh ORDER BY trong sub query, mặc dù truy vấn chính có thể sử dụng ORDER BY. Lệnh GROUP BY có thể được sử dụng để thực hiện chức năng giống như ORDER BY trong một sub query.
   - Sub query trả về nhiều hơn một hàng chỉ có thể được sử dụng với toán tử nhiều giá trị như toán tử IN.
   - Một sub query không thể được chứa trực tiếp một chức năng set.
   - Toán tử BETWEEN không thể được sử dụng với một sub query. Tuy nhiên, toán tử BETWEEN có thể được sử dụng trong sub query.

```sql 
/* lay fullname  tu bang tbl_admin thoa man co id nam trong cot creator cua bang tbl_post*/
 SELECT fullname FROM app.tbl_admin WHERE id IN  (SELECT creator FROM app.tbl_post); 
  /*Tuuong tu nhu cu phap duoi *
  SELECT DISTINCT fullname FROM app.rbl_admin INNER JOIN app.tbl_post ON tbl_admin.id = tbl_post>creator 
  
  SELECT fullname FROM app.tbl_admin WHERE id = ANY ( SELECT creator FROM app.tbl_post) 
  
  
```
#### Joins 
  
 Trong SQL, một mệnh đề JOIN được sử dụng để trả về tập kết quả cái mà kết nối dữ liệu từ nhiều bảng,
dựa trên 1 cột chung cái mà được thiết lập ở cả hai bảng.  

 Có các các joins khác nhau cho bạn sử dụng: 
 
  - Inner Join ( mặc định ): Trả về bất kỳ bản ghi nào cái mà khớp giá trị giữa các bảng.
  - left join: Trả về tất cả các bản ghi của bảng đầu tiên và bất kỳ bản ghi nào khớp từ bảng thứ hai. 
  - Right join: Trả về tất cả các bản ghi từ bảng thứ hai và bất kỳ giá trị nào khớp từ bảng đầu tiên. 
  - Full join: Trả về tất cả các bản ghi từ cả hai bảng khi có 1 bản khớp. 


```sql 
   /*Lay fullname o bang admin va post_title o bang post khi co su phu hop*/
   SELECT tbl_admin.fullname, tbl_post.post_title FROM app.tbl_admin INNER JOIN app.tbl_product ON tbl_admin.id = tbl_product.creator;
```

##### index 

Index là một trong những yếu tố quan trọng nhất góp phần vào việc nâng cao hiệu suất của cơ sở dữ liệu. Index trong SQL tăng tốc độ của quá trình truy vấn dữ liệu bằng cách cung cấp phương pháp truy xuất nhanh chóng tới các dòng trong các bảng, tương tự như cách mà mục lục của một cuốn sách giúp bạn nhanh chóng tìm đến một trang bất kỳ mà bạn muốn trong cuốn sách đó.

**Lưu ý khi dùng index**: 
- Các chỉ mục không nên dùng trên các bảng nhỏ 
- Bảng mà thường xuyên có hoạt động update, insert 
- Các chỉ mục không nên được sử dụng trên các cột có phần lớn giá trị null
- Không nên dùng chỉ mục trên các cột có dữ liệu thường xuyên thay đổi. 


#### Transaction 

Transaction trong SQL là một nhóm các câu lệnh SQL. Nếu transaction được thực hiện thành công, tất cả các thay đổi dữ liệu được thực hiện trong transaction sẽ được lưu vào cơ sở dữ liệu.
Nếu 1 transaction  bị lỗi và rollback, dữ liệu thay đổi sẽ bị xóa ( dữ liệu được khôi phục lại trạng thái ban đầu khi chưa được transaction)  

 **Transaction có 4 đặc điểm sau**:
- Atomicity: Một transaction xác định ranh giới của nó rất rõ ràng, tức xác định điểm bắt đầu và kết thúc của tiến trình. Như vậy có thể coi nó như một đơn vị thực thi và đơn vị thực thi này thực hiện theo nguyên tắc “all or nothing”. Nghĩa là nếu một thành phần nào đó trong transaction thực thi lỗi thì đồng nghĩa với việc không có gì xảy ra tức không có gì thay đổi về mặt dữ liệu.
- Consistency: Dữ liệu nhất quán với transaction ở thời điểm bắt đầu và kết thúc hay bảo đảm rằng Database thay đổi một cách chính xác trạng thái theo một transaction đã được commit thành công.
- Isolation: Các transaction có khả năng hoạt động một cách độc lập và không liên quan đến nhau.
- Durability: Dữ liệu của transaction sau khi thực thi xong được cố định, chính thức và bền vững. Nghĩa là những thay đổi đã được cố định, không có chuyện có thể chuyển lại trạng thái dữ liệu lúc trước khi thực hiện transaction.

**Xử lý transaction**
- COMMIT : Để lưu các thay đổi 
- ROLLBACK: Để khôi phục các thay đổi.
- SAVEPOINT: Tạo ra các điểm trong transaction để ROLLBACK 
- SET TRANSACTION : Thiết lập các thuộc tính cho transaction 

Các lệnh điều khiển transaction chỉ được sử dụng với các lệnh thao tác dữ liệu DML như - INSERT, UPDATE và DELETE.

#### PDO 

- PHP Data Objects (PDO) là một lớp truy xuất cơ sở dữ liệu cung cấp một phương pháp thống nhất để làm việc với nhiều loại cơ sở dữ liệu khác nhau. Khi làm việc với PDO bạn sẽ không cần phải viết các câu lệnh SQL cụ thể mà chỉ sử dụng các phương thức mà PDO cung cấp, giúp tiết kiệm thời gian và làm cho việc chuyển đổi Hệ quản trị cơ sở dữ liệu trở nên dễ dàng hơn, chỉ đơn giản là thay đổi Connection String (chuỗi kết nối CSDL).
- Chỉ cần nắm rõ các API mà PDO cung cấp để có thể làm việc với nhiều Hệ quản trị CSDL khác nhau. 


**kết nối CSDL**

Mỗi DBMS sẽ có các phương thức kết nối khác nhau (có loại cần Username, Password, đường dẫn đới Database, Port, có loại không). Connection String của các DBMS phổ biến hầu hết đều có dạng như sau:
  
 Đối với Mysql: 
```php
 $conn = new PDO('mysql:host=localhost;dbname=izlearn', $username, $password);
```

 Đối với SQLlite: 
```php
$conn = new PDO("sqlite:your/database/path/izlearn.db");
```

 **Để ngắt kết nối**: `$conn = null`
 
**insert** và **update**: 
  
Với mỗi hoạt động Insert hay update đưowjc chia làm 3 quá trình sử dụng cơ chế Prepare Statement 
- Prepare statement: Chuẩn bị một câu lệnh SQL làm khung/mẫu được gọi là Prepared Statement với các Placeholder (có thể hiểu placeholder đóng vai trò như tham số của các phương thức khi bạn khai báo hàm)
- Bind params: Gắn giá trị thực vào các placeholder (tương tự như khi bạn truyền giá trị vào các tham số của phương thức)
- Execute: Thực thi câu lệnh.

**select** 

Khi đọc dữ liệu từ database, PDO sẽ trả về dữ liệu theo cấu trúc mảng (array) hoặc đối tượng (object) thông qua phương thức fetch(). Bạn nên thiết lập trước cấu trúc dữ liệu trước khi gọi phương thức này, PDO hỗ trợ nhiều tùy chọn khác nhau. 

- PDO::FETCH_ASSOC: Trả về dữ liệu dạng mảng với key là tên của column (column của các table trong database)
- PDO::FETCH_BOTH (default): Trả về dữ liệu dạng mảng với key là tên của column và cả số thứ tự của column
- PDO::FETCH_CLASS: Gán giá trị của từng column cho từng thuộc tính (property/attribute) của một lớp Class theo tên column và tên thuộc tính.
-  PDO::FETCH_INTO: Gán giá trị của từng column cho từng thuộc tính của một Class Instance (thể hiện của một lớp)
- PDO::FETCH_LAZY: Gộp chung PDO::FETCH_BOTH/PDO::FETCH_OBJ
- PDO::FETCH_NUM: Trả về dữ liệu dạng mảng với key là số thứ tự của column
- PDO::FETCH_OBJ: Trả về một Object của stdClass (link is external) với tên thuộc tính của Object là tên của column.


 Trong đó thường sử dụng: FETCH _ASSCOC, FETCH_CLASS và FETCH_OBJ

Để thiết lập cấu trúc dữ liệu (Fetch Style hay Fetch Mode) trước khi fetch ta dùng câu lệnh sau:

```php 
$stmt->setFetchMode(PDO::FETCH_ASSOC);
```
Hoặc cũng có thể sử dụng khi gọi phương thức fetch():
```php
$stmt->fetch(PDO::FETCH_ASSOC);
```
Demo 
  
```php 
//Tạo Prepared Statement
$stmt = $conn->prepare('SELECT email, age from users WHERE name = :name');

//Thiết lập kiểu dữ liệu trả về, chỉ định dữ liệu được đưa vào object của class User
$stmt->setFetchMode(PDO::FETCH_CLASS, 'User');

//Gán giá trị và thực thi
$stmt->execute(array('name' => 'a'));

//Hiển thị kết quả, vòng lặp sau đây sẽ dừng lại khi đã duyệt qua toàn bộ kết quả trả về
while($obj = $stmt->fetch()) {
    echo $obj->email;
    echo $obj->isAdmin;
}

```

Đối với các lệnh SQL không có dữ liệu trả về, và không cần thiết phải truyền tham số thì có thể sử dụng phương thức exec(). Phương thức này sẽ trả về số lượng row bị tác động sau khi thực hiện câu lệnh. Như ví dụ trên sẽ trả về số lượng row bị xoá.


**eceptions**
PDO dùng các Exceptions để xử lý các lỗi phát sinh khi làm việc với database, vì thế tất cả những gì bạn làm với PDO nên được đặt trong một try/catch block. PDO cung cấp 3 chế độ xử lý lỗi (Error Mode) được thiết lập thông qua phương thức setAttribute():

```php
$conn->setAttribute( PDO::ATTR_ERRMODE, PDO::ERRMODE_SILENT );
$conn->setAttribute( PDO::ATTR_ERRMODE, PDO::ERRMODE_WARNING );
$conn->setAttribute( PDO::ATTR_ERRMODE, PDO::ERRMODE_EXCEPTION );
```
- **PDO::ERRMODE_SILENT**: Đây là chế độ xử lý lỗi mặc định của PDO, khi gặp mỗt lỗi bất kỳ, PDO sẽ im lặng (silent) và chương trình vẫn tiếp tục chạy. Bạn có thể lấy mã lỗi và thông tin về các lỗi đã xảy ra qua PDO::errorCode() và PDO::errorInfo()
- **PDO::ERRMODE_WARNING**: Ở chế độ này khi gặp phải lỗi PDO sẽ ném ra một PHP Warning, chương trình sẽ tiếp tục chạy.
- **PDO::ERRMODE_EXCEPTION**: Đây là mode nên sử dụng nhất, khi đặt trong một try/catch block sẽ giúp bạn kiểm soát các lỗi phát sinh một cách uyển chuyển và giấu các thông báo lỗi có thể khiến Attacker khai thác hệ thống của bạn.


#### SQL Injection 
 
SQL injection là 1 kỹ thuật tiêm mã có  thể phá hủy cơ sở dữ liệu của bạn.  

SQL injection là 1 trong những kỹ thuật hack web phổ biến nhất   

SQL injection là vị trí của mã độc trong các câu lệnh của SQL, thông qua đầu vào.

SQL injection thường xảy ra khi yêu cầu 1 người dùng nhập đầu vào, như tên đăng nhập/id, và họ không nhập tên/id, họ cung cấp 1 câu lệnh SQL cái mà bạn không biết nó chạy trên CSDL của bạn. 

```php 
$username  = $_POST['username'];

$sql = "SELECT * FROM tbl_admin WHERE username = " + $username;
// Nếu người dùng nhập trường username = 'amdin OR 1 = 1';
//câu truy vấn sẽ là: $sql = "SELECT * FROM tbl_admin WHERE username = admin OR 1 = 1"
  câu lệnh này sẽ trả về tất cả các bản ghi vì mệnh đề WHERE luôn đúng. 
  
  // Có thể xóa bảng dữ liệu : 
  // Nếu người dùng nhập trường username = '105; DROP TABLE Users';

  $username = 101; DROP TABLE Users;
  
```

 Cách giảm thiểu và phòng ngừa SQL injection: 

- Luôn kiểm tra kỹ các trường nhập dữ liệu và các bạn cần ràng buộc thật kỹ dữ liệu người dùng nhập vào.
- Dùng Regular Expression để loại bỏ đi các ký tự lạ hoặc các ký tự không phải là số.
- Hoặc dùng các hàm có sẵn để giảm thiểu lỗi. Mỗi khi truy vấn thì mọi người nên sử dụng thêm hàm mysqli_real_escape_string để chuyển đổi một chuỗi thành một query an toàn.  






