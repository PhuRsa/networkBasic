HTTP REQUESTS

- Khái Niệm : HTTP request là thông tin được gửi từ client lên server, để yêu cầu server tìm hoặc xử lý một số thông tin, dữ liệu mà client muốn. HTTP request có thể là một file text dưới dạng XML hoặc Json mà cả hai đều có thể hiểu được.

Các Phương Thức Của HTTP_request:

- METHOD GET : 
  Get là phương thức được Client gửi dữ liệu lên Server thông qua đường dẫn URL nằm trên thanh địa chỉ của Browser. Server sẽ nhận đường dẫn đó và phân tích trả về kết quả cho bạn. Hơn nữa, nó là một phương thức được sử dụng phổ biến mà không cần có request body.

- Ví dụ điển hình là khi bạn mở một trang web, Client sẽ gửi một phương thức Get lên server để truy xuất nội dung hiển thị của trang web. Nó tương đương với thao tác đọc.

Một số đặc điểm chính của phương thức Get là:

Giới hạn độ dài của các giá trị là 255 kí tự.
- Chỉ hỗ trợ các dữ liệu kiểu String.
- Có thể lưu vào bộ nhớ cache.
- Các tham số truyền vào được lưu trữ trong lịch sử trình duyệt.
- Có thể được bookmark (đánh dấu rồi xem lại sau) do được lưu trong lịch sử trình duyệt.

  METHOD POST:Phương thức gửi dữ liệu đến server giúp bạn có thể thêm mới dữ liệu hoặc cập nhật dữ liệu đã có vào database.Chúng ta sẽ gửi thông tin cần thêm hoặc cập nhật trong phần body request.

Một số đặc điểm chính của Post là:

- Dữ liệu cần thêm hoặc cập nhật không được hiển thị trong URL của trình duyệt.
- Dữ liệu không được lưu trong lịch sử trình duyệt.
- Không có hạn chế về độ dài của dữ liệu.
- Hỗ trợ nhiều kiểu dữ liệu như: String, binary, integers,..

  METHOD PUT:Cách hoạt động tương tự như Post nhưng nó chỉ được sử dụng để cập nhật dữ liệu đã có trong database. Khi sử dụng nó, bạn phải sửa toàn bộ dữ liệu của một đối tượng.
PUT & POST : POST method để tạo một address mới và lưu xuống database. PUT method dùng để cập nhật một address đã tồn tại trước đó dựa theo ID kèm theo, nếu không tìm thấy nó sẽ tạo một address mới.

  METHOD PATCH:Tượng tự như Post và Put, nhưng Patch được sử dụng khi phải cập nhật một phần dữ liệu của đối tượng.

  METHOD DELETE:khi sử dụng phương thức Delete sẽ xoá các dữ liệu của server về tài nguyên thông qua URI. Cũng giống như GET, phương thức này không có body request.

  METHOD HEAD: HEAD gần giống giống với lại GET, tuy nhiên nó không có response body.

  Nói một cách khác, nếu sử dụng phương thức GET tới đường dẫn /Books thì sẽ trả về danh sách các sản phẩm, còn khi sử dụng HEAD tới đường dẫn /Books nhưng không nhận được danh sách các sản phẩm.

  Truy vấn HEAD hữu ích khi chúng ta sử dụng nó để kiểm tra API có hoạt động không do không có response body nên thời gian phản hồi nhanh hơn so với phương thức Get. Và thường được sử dụng để kiếm tra trước khi download file do cứ gọi đến api dowload sẽ download file nên thêm phương thức head vào nó kiểm tra xem api có đang hoạt động tốt không tránh down nhiều.
- STRUCTURE HTTP REQUEST :
Một HTTP request bao gồm:

- Request line
- Body request ( có thể có hoặc không)
REQUEST LINE :

- Request line là dòng đầu tiên trong HTTP request. Nó bao gồm 3 phần:
- Phương thức HTTP được sử dụng
- URI( Uniform Resource Identifier) giúp xác định các tài nguyên mà client yêu cầu.
- Phiên bản của giao thức HTTP
VÍ DỤ : Một request line sẽ có định dạng như sau: GET /BookStore/v1/Books HTTP/1.1

REQUESST HEADER :
- Request header giúp client có thể gửi yêu cầu lên server. Mỗi yêu cầu sẽ kèm theo các thông số, và các thông số đó được gọi là Header Parameters. Trình duyệt và server sẽ dựa vào các thông số header này để trả dữ liệu và hiển thị dữ liệu cho phù hợp.
Các thông số mà các bạn có thể gặp khá thường xuyên như:

- User-Agent: cho phép server xác định ứng dụng, hệ điều hành, nhà cung cấp và phiên bản.
- Connection: kiểm soát kết nối mạng. Nói cách khác, cho phép dừng hoặc tiếp tục kết nối sau khi server thực hiện xong yêu cầu.
- Cache-Control: chỉ định chính sách bộ nhớ đệm của trình duyệt.
- Accept-Language: cho biết tất cả các ngôn ngữ (tự nhiên) mà client có thể hiểu được.
- Host: Trường này xác định tên miền hoặc địa chỉ IP của máy chủ web mà yêu cầu được gửi đến.
- Authorization: Trường này chứa thông tin xác thực người dùng (username và password) để truy cập vào các trang web bảo mật.
- Cookie: Trường này chứa các cookie được gửi đến từ trình duyệt của người dùng. Cookie được sử dụng để lưu trữ thông tin về người dùng và các thông tin khác như thông tin giỏ hàng, lịch sử truy cập, v.v.
- Referer: Trường này chỉ ra địa chỉ URL của trang web mà yêu cầu được gửi từ đó.
.....

REQUEST BODY :
Cho phép client gừi đến yêu cầu bổ sung cần server thực hiện như: tạo mới hoặc cập nhật dữ liệu mà không thể truyền trên Header Parameters.

Request body thường được sử dụng trong các phương thức Post, Put, Patch.

RESPOND HEADER :
  HTTP Response Header là các thông tin được gửi từ máy chủ web đến trình duyệt của người dùng như phản hồi cho một yêu cầu HTTP Request. Header này chứa các thông tin về nội dung trả về, thông tin về máy chủ, thông tin về mã trạng thái và các thông tin khác liên quan đến phản hồi.

Các trường header thông thường bao gồm:

- Date: Chứa thời gian máy chủ phản hồi yêu cầu.
- Server: Chứa thông tin về mã và phiên bản của máy chủ web.
- Content-Type: Chứa thông tin về định dạng của nội dung trả về (ví dụ: text/html).
- Content-Length: Chứa thông tin về kích thước của nội dung trả về.
- Cache-Control: Chứa các chỉ thị về bộ nhớ đệm cho các trình duyệt để giảm tải tài nguyên của máy chủ.
- Expires: Chứa thời gian hết hạn của nội dung được lưu trữ trong bộ nhớ đệm của trình duyệt.
- Location: Chứa địa chỉ URL mới nếu phản hồi là một chuyển hướng (redirect).
- Set-Cookie: Chứa các thông tin về cookie được thiết lập cho trình duyệt.
- Content-Encoding: Chứa thông tin về phương thức nén được sử dụng cho nội dung trả về (ví dụ: gzip).

  Thông tin từ Response Header giúp trình duyệt hiểu được nội dung và các thông tin liên quan đến phản hồi, giúp cho quá trình truyền tải nội dung được diễn ra một cách hiệu quả và đáp ứng được yêu cầu của người dùng.
