# Cách Tạo một YIP

## Tóm tắt

Đề xuất Cải thiện yEarn \(`YIP`\) mô tả các quy cách phát triển nền tảng yEarn, từ thông số kỹ thuật của giao thức cốt lõi, giao diện lập trình ứng dụng máy khách (`client API`) đến tiêu chuẩn hợp đồng (`contract`). Đây là tư liệu đặc tả mang tính quyết định, `chính thống` nhất cho lô-gic cốt lõi.

## Đóng góp

1. Đọc kỹ [YIP-0](https://github.com/yearn/YIPS/blob/master/YIPS/yip-0.md).
2. "Rẽ nhánh" (`Fork`) tập mã nguồn (`repository` hay `repo`) nói trên bằng cách click nút "Fork" ở góc trên bên phải.
3. Thêm YIP của bạn vào tập mã nguồn vừa rẽ nhánh của mình. Xem [bản mẫu YIP tại đây](https://github.com/yearn/YIPS/blob/master/yip-X.md).
4. Gửi một "Pull Request" (hay viết tắt là "PR") cho [tập mã nguồn YIP](https://github.com/yearn/YIPS/) của yEarn.

PR đầu tiên của bạn nên là bản thảo thứ nhất của YIP hoàn chỉnh. Nó phải đáp ứng được các tiêu chuẩn định dạng mà trình tạo lập (`build`) yêu cầu \(tiêu đề lớn, chứa đúng siêu dữ liệu—`metadata`\). Một biên tập viên sẽ đích thân kiểm tra PR đầu tiên của YIP mới và gán số hiệu trước khi gộp (`merge`) nó vào. Đừng quên bao gồm một tiêu đề `discussions-to` với URL (liên kết) trỏ đến nơi mọi người có thể cùng thảo luận tương ứng trên diễn đàn quản trị [gov.yearn.finance](https://gov.yearn.finance/).

> Chú ý: Điều quan trọng là `YIP` được đề xuất phải có sự hậu thuẫn của cộng đồng. Trách nhiệm thuộc về tác giả để "định hướng" và thu thập sự hưởng ứng cho đề xuất của mình xuyên suốt quá trình này.

Nếu YIP cần hình ảnh, chúng nên được thêm vào nhánh phụ (`subdirectory`) của thư mục "tài sản" (`assets`) cho YIP đó như sau: `assets/yip-X` \(cho yip **X**\). Khi đưa hình ảnh vào YIP, hãy sử dụng liên kết tương đối như `../assets/yip-X/image.png`.

Khi thấy YIP của mình đã đầy đủ và sẵn sàng kết thúc pha WIP (viết tắt "Work In Progress", nghĩa là "đang trong công đoạn sửa đổi, hoàn thiện"), bạn có thể yêu cầu đưa nó vào thảo luận ở cuộc họp quản trị tiếp theo, nhằm được duyệt vào nội dung nâng cấp nền tảng trong tương lai gần. Nếu cộng đồng chấp thuận, soạn viên YIP sẽ cập nhật trạng thái YIP của bạn thành "Đã được duyệt".

## Trạng thái YIP

- **WIP** - YIP vẫn đang được phát triển.
- **Đã đề xuất** - YIP sẵn sàng cho giai đoạn đánh giá khi họp quản trị.
- **Đã được duyệt** - YIP đã được cộng đồng yEarn chấp thuận để thực hiện.
- **Đã được thực hiện** - YIP đã được phát hành trên mạng chính (mainnet).
- **Đã bị phản đối** - YIP đã bị phản đối và bác bỏ.

### Thí dụ YIP

```diff
-Trạng thái: Đã đề xuất
+Trạng thái: Đã được duyệt
YIP: số nguyên,
Được tạo: 2020-09-01
-Sửa đổi gần nhất: 2020-09-03
+Sửa đổi gần nhất: 2020-09-08
```

## Hợp thức hóa

YIP PHẢI vượt qua một số tiêu chuẩn hợp thức hóa. Tập mã nguồn (repository) của YIP đảm bảo điều này bằng cách chạy kiểm định sử dụng [html-proofer](https://rubygems.org/gems/html-proofer) và [yip_validator](https://rubygems.org/gems/yip_validator).

Bạn có thể chạy trình kiểm định YIP cục bộ (nội trong môi trường máy tính của mình):

```ruby
gem install yip_validator
yip_validator <INPUT_FILES>
```

## Bản quyền

Không có bản quyền hay bất cứ quyền liên quan nào theo [CC0](https://creativecommons.org/publicdomain/zero/1.0/), [wiki Tiếng Việt có giải thích](https://vi.wikipedia.org/wiki/Creative_Commons).
