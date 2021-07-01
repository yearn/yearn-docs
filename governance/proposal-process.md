# Quá trình Đề xuất

Hệ sinh thái Yearn nằm dưới sự kiểm soát của những người chủ sở hữu tôken YFI. Họ có toàn quyền đệ trình và biểu quyết các đề xuất ngoại-chuỗi ("off-chain") để quản trị hệ sinh thái. Những đề xuất mà đa số ủng hộ (>50% số lượng biểu quyết) sẽ được hiện thực hóa bởi 9 thành viên của Ví Đa-ký (Ví chung, "Multisig" hay "multi-signature wallet"). 

Các thay đổi phải được ký bởi 6 trên 9 thành viên Ví chung (Multisig) nếu muốn trở thành hiện thực. [Thành viên Ví Đa-ký](https://docs.yearn.finance/resources/faq#who-is-on-the-multisig) do chủ sở hữu đồng YFI bầu lên, và có thể thay đổi khi biểu quyết quản trị về vấn đề này xuất hiện trong tương lai.

# Thảo luận

Thảo luận về các thay đổi trong giao thức diễn ra ở nhiều nền tảng như:

 - [Diễn đàn Quản trị](https://gov.yearn.finance/)
 - [Discord (có kênh riêng cho Tiếng Việt)](https://discord.yearn.finance)
 - [Telegram](https://t.me/yearnfinance)

Hãy khảo sát phản ứng cũng như thu thập nhiều góp ý nhất có thể ở những kênh thảo luận trên trước khi đăng tải đề xuất chính thức. Diễn đàn quản trị và máy chủ Discord có kênh dành riêng cho các chủ đề cụ thể.

# Đề xuất

## Các loại đề xuất

**Đề xuất Cải thiện Yearn** (YIP) là cách chung để chủ sở hữu tôken thực thi quyền lợi của mình. Sau [YIP-61](https://gov.yearn.finance/t/yip-61-governance-2-0/10460), **Đề xuất Ủy quyền Yearn** (YDP) ra đời, cho phép chủ tôken thay đổi bất cứ quyền quyết-định-riêng nào được ủy thác.

![](https://i.imgur.com/ZRNp2Zq.png)

### Lịch sử và các đề xuất hiện tại
- Lịch sử: [Tổng hợp các đề xuất](https://docs.yearn.finance/governance/proposal-repository)
- Hiện tại: [Snapshot](https://snapshot.page/#/yearn) 

### Điều kiện để duyệt và thông qua đề xuất
- 3 ngày thảo luận trên [diễn đàn](https://gov.yearn.finance/)
  - Ít nhất 25% biểu quyết "tán thành" thay đổi
- Sở hữu 1 đồng YFI để gửi Snapshot
- 5 ngày [Snapshot](https://snapshot.org/#/ybaby.eth) với hơn 50% biểu quyết thông qua

## Tạo đề xuất

Ai cũng có quyền đăng tải một đề xuất lên diễn đàn để thảo luận nội trong cộng đồng. Nếu nó được lên cấp biểu quyết ngoại-chuỗi (qua [Snapshot](https://snapshot.page/#/yearn)), chỉ người nào sở hữu 1 đồng YFI mới có thể gửi cho Snapshot. Trong trường hợp không có đủ YFI, các quản trị viên (mod) sẽ giúp bạn.

Bản mẫu mặc định cho đề xuất có tại [Github](https://github.com/yearn/YIPS/blob/master/yip-X.md) + trên [diễn đàn](https://gov.yearn.finance) nếu bạn viết bài dưới mục đề xuất hay chỉ cần thảo luận, nó cũng sẽ được tự động điền theo mẫu.

**Tham khảo thêm**:
- [Hướng dẫn Đề xuất](https://gov.yearn.finance/t/proposal-how-to/106)
- [YIP 0: Mục tiêu và Đường lối của YIP](https://yips.yearn.finance/YIPS/yip-0)
- [YIP 44: Cải thiện các loại YIP](https://yips.yearn.finance/YIPS/yip-44)
- [YIP 55: Chính thức hóa YIP và Tiến trình Biểu quyết](https://gov.yearn.finance/t/yip-55-formalize-the-yip-process/7959)

# Biểu quyết

## Làm sao để biểu quyết?

- Nắm giữ hoặc "cầm cắm" (đặt cọc; "stake" trong tiếng Anh) đồng YFI ở những nơi sau sẽ cho phép bạn biểu quyết trên trang [Snapshot](https://snapshot.page/#/yearn) của Yearn:
	- Ví riêng của mình
	- Kho bạc "YFI yVault V2" (tương đương với việc nắm giữ tôken yvYFI)
	- Tôken LP (cấp thanh khoản) của cặp YFI/WETH ở Balancer
	- Tôken LP (cấp thanh khoản) của cặp YFI/WETH ở Uniswap
	- Tôken LP (cấp thanh khoản) của cặp YFI/WETH ở Sushiswap và được "cầm cắm" trong "MasterChef"
	- Thế chấp YFI ở MakerDAO
	- Thế chấp YFI ở Unit Protocol
	- Bancor

## Có gì khác nhau giữa biểu quyết khảo sát trên diễn đàn với biểu quyết ngoại-chuỗi (off-chain)?

- Một cuộc khảo sát chỉ nhằm đánh giá sơ bộ phản ứng của cộng đồng về đề xuất, trong khi biểu quyết ngoại-chuỗi (off-chain) (qua [Snapshot](https://snapshot.page/#/yearn)) mang tính bắt buộc hơn và sẽ có hiệu lực nếu được duyệt thông qua.

# Hiện thực hóa

Sau khi biểu quyết Snapshot duyệt thông qua, các thay đổi sẽ thành hiện thực nhờ công đoạn của giao thức Yearn hoặc ê-kíp vận hành và được ký giao tác trực-chuỗi (on-chain) bởi Ví chung (Multisig), nếu cần.
