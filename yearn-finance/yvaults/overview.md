# Tổng quan

## yVault là gì?

[yVault](https://yearn.finance/vaults) (hay Vault—Kho bạc) giống như tài khoản tiết kiệm cho tài sản mã thuật số (crypto). Chúng chấp nhận khoản ký gửi của bạn, sau đó luân chuyển tiền qua nhiều chiến lược (dựa trên hàng loạt 'hợp đồng thông minh') nhằm chọn ra nơi nào mang lại lãi suất cao nhất trong DeFi.

![](https://i.imgur.com/yXnJqsn.png)

## 'Zap' vào với bất cứ tài sản nào 

Nhờ [Zapper](https://zapper.fi/), việc ký gửi vào các yVault trở nên vô cùng dễ dàng. Miễn là bạn sở hữu tôken có thể bán đổi được trên Uniswap mà không trượt giá quá 1%, Vault (Kho bạc) sẽ chấp nhận tôken đó, quy đổi sang những gì cần thiết cho kho này và ký gửi vào, tất cả gói gọn trong cùng một giao dịch.

Khi rút, người dùng sẽ có thể 'zap' trở lại thành một trong những tôken sau: 
- ETH, WETH, DAI, USDT, USDC, WBTC

## Cấu trúc Phí của yVault

|Phiên bản yVault|Phí Rút|Phí Thành quả|Phí Quản lý|
|--------------|:-----------:|:-------------:|:------------:|
|v1|0.5%|5%|-|
|v2|-|20%|2%|

- Phí Rút: Phí một-lần lúc rút
- Phí Thành quả: Phần trăm trừ đi từ thu nhập
- Phí Quản lý: Phần trăm trừ đi từ tổng số dư hàng năm.

## Các Cải tiến ở yVault v2

- **Lên đến 20 chiến lược mỗi Vault (Kho bạc):** Điều này sẽ nâng cao tính linh hoạt để quản lý vốn hiệu quả hơn trong nhiều tình huống thị trường khác nhau. Mỗi chiến lược có giới hạn số vốn tối đa, giúp tránh việc phân bổ quá nhiều tiền vào một chiến lược không còn khả năng tăng thêm APY (Phần Trăm Lãi Suất Hàng Năm) nữa.
- **Chiến lược gia và Giám hộ là Kiểm soát viên mới:** Khái niệm Kiểm soát viên không còn áp dụng cho các yVault V2 và được thay thế bằng một Giám hộ cũng như tác giả của Chiến lược \(chiến lược gia \). Hai người này sẽ theo dõi hiệu suất của chiến lược và được quyền hành động để cải thiện quản lý vốn, hoặc xử trí trong những tình huống nghiêm trọng.
- **Quản kho tự động \(Keep3r network\):** Gọi `harvest()` và `earn()` giờ sẽ tự động hóa qua mạng lưới rô-bốt Keep3r. Hai hàm gọi này dùng để mua tài sản thế chấp cơ sở mới bằng cách bán tôken thu hoạch được trong khi chuyển lợi nhuận trở lại Vault (Kho bạc) và sau đó vào các chiến lược. Mạng Keep3r nhận gánh nặng thực hiện những tác vụ gọi đó cũng như phí gas để đổi lấy tôken Keep3r. Giải pháp này giảm tải cho con người khỏi các tác vụ vặt.
- **Bảo vệ và danh sách Khách mời**: Yearn đã tạo quá trình phát triển Vault (Kho bạc) mới rất độc đáo. Mọi kho được bắt đầu bằng Vault Thử nghiệm \(tyvToken\). Vault Thử nghiệm có giới hạn tối đa, áp dụng cho cả chiến lược trong đó. Đồng thời, Bảo vệ (Bouncer) có danh sách khách mời (những địa chỉ ví) được phép tương tác (ký gửi và rút vốn) với Vault Thử nghiệm. Giải pháp này ngăn ngừa những người dùng không biết rõ, giúp họ tránh mất tiền vô ích vào một sản phẩm chưa hoàn thiện.
