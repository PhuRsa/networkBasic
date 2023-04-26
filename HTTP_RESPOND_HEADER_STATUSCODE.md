  HTTP Response (Phản hồi HTTP) là một thông điệp trả lại từ máy chủ web cho trình duyệt của người dùng sau khi nhận được một yêu cầu từ trình duyệt. Phản hồi này bao gồm một mã trạng thái HTTP và một nội dung phản hồi.

  Mã trạng thái HTTP (HTTP status code) là một mã số ba chữ số được sử dụng để xác định kết quả của yêu cầu. Các mã trạng thái phổ biến nhất trong HTTP bao gồm:

- 1xx (Thông tin): Thông tin về yêu cầu đã được tiếp nhận và đang được xử lý.
- 2xx (Thành công): Yêu cầu đã được xử lý thành công và trả về kết quả đúng.
- 3xx (Chuyển hướng): Yêu cầu cần phải được chuyển hướng để hoàn tất.
- 4xx (Lỗi từ phía người dùng): Yêu cầu chứa lỗi từ phía người dùng, ví dụ như sai cú pháp hoặc yêu cầu không hợp lệ.
- 5xx (Lỗi từ phía máy chủ): Yêu cầu chứa lỗi từ phía máy chủ, ví dụ như máy chủ bị lỗi hoặc quá tải.

  Nội dung phản hồi HTTP (HTTP response body) chứa thông tin được trả về từ máy chủ web, như là HTML, JSON, XML hoặc các loại dữ liệu khác phù hợp với loại yêu cầu. Nội dung này được trả về dưới dạng một chuỗi ký tự.

  Phản hồi HTTP là một phần quan trọng trong quá trình giao tiếp giữa trình duyệt và máy chủ web, giúp đảm bảo rằng các yêu cầu được xử lý một cách chính xác và trả về đầy đủ thông tin cần thiết cho người dùng.
  
  RESPOND HEADER : HTTP Response Header là các thông tin được gửi từ máy chủ web đến trình duyệt của người dùng như phản hồi cho một yêu cầu HTTP Request. Header này chứa các thông tin về nội dung trả về, thông tin về máy chủ, thông tin về mã trạng thái và các thông tin khác liên quan đến phản hồi.

Các trường header thông thường bao gồm:

- Date: Chứa thời gian máy chủ phản hồi yêu cầu.
- Server: Chứa thông tin về mã và phiên bản của máy chủ web.
- Content-Type: Chứa thông tin về định dạng của nội dung trả về (ví dụ: text/htm
- Content-Length: Chứa thông tin về kích thước của nội dung trả về.
- Cache-Control: Chứa các chỉ thị về bộ nhớ đệm cho các trình duyệt để giảm tải tài nguyên của máy chủ.
- Expires: Chứa thời gian hết hạn của nội dung được lưu trữ trong bộ nhớ đệm của trình duyệt.
- Location: Chứa địa chỉ URL mới nếu phản hồi là một chuyển hướng (redirect).
- Set-Cookie: Chứa các thông tin về cookie được thiết lập cho trình duyệt.
- Content-Encoding: Chứa thông tin về phương thức nén được sử dụng cho nội dung trả về (ví dụ: gzip).

Thông tin từ Response Header giúp trình duyệt hiểu được nội dung và các thông tin liên quan đến phản hồi, giúp cho quá trình truyền tải nội dung được diễn ra một cách hiệu quả và đáp ứng được yêu cầu của người dùng.
