Chức năng


Method


URL


Query params (nếu có)


Status thành công


Status lỗi (ví dụ)


Lấy danh sách sách (có phân trang & lọc theo tác giả)


GET


/books


?page=1&limit=10&author=…


200 OK


400 Bad Request (tham số không hợp lệ)


Thêm sách mới


POST


/books


–


201 Created


400 Bad Request (body thiếu field bắt buộc)


Lấy chi tiết 1 sách


GET


/books/{id}


–


200 OK


404 Not Found (không tồn tại sách với id)


Cập nhật số lượng sách (chỉ 1 trường)


PATCH


/books/{id}


–


200 OK


400 Bad Request (quantity âm) / 404 Not Found


Xóa sách


DELETE


/books/{id}


–


204 No Content


404 Not Found (sách không tồn tại)


Lấy danh sách thẻ mượn của một sách (sub-resource)


GET


/books/{bookId}/loans


?page=1&limit=10


200 OK


404 Not Found (bookId không tồn tại)


Tạo thẻ mượn mới


POST


/loans


–


201 Created


400 Bad Request (bookId không hợp lệ hoặc hết sách)


Lấy chi tiết 1 thẻ mượn


GET


/loans/{id}


–


200 OK


404 Not Found (loan không tồn tại)


Trả sách (cập nhật ngày trả)


PATCH


/loans/{id}


–


200 OK


400 Bad Request (đã trả rồi) / 404 Not Found


Lấy danh sách thẻ mượn theo người mượn


GET


/loans


?borrowerName=Huy&page=1&limit=10


200 OK


400 Bad Request (tham số sai định dạng)







