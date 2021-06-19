# Yearn tăng lợi tức cho bạn bằng cách nào?

Gần như mọi thứ (mà yVault tương tác với) đều công khai. Vậy, tại sao Yearn mang lại lợi tức lớn hơn so với khi người dùng tự làm?

## Hợp tác với Curve Finance

Rất nhiều chiến lược của Yearn tận dụng kế hoạch 'khai thác thanh khoản' (liquidity mining) của giao thức Curve Finance. [Curve Finance](https://curve.fi/) có chương trình phân phát tôken lâu 300 năm nhằm khuyến khích dài hạn cho những bên cung cấp thanh khoản ở sàn giao dịch phi-tập-trung, trượt-giá-thấp của họ.

### Kích veCRV 

Đồng CRV được phân phát liên tục cho những bên 'đặt cọc' một số tôken bảo-chứng-thanh-khoản ('liquidity provider token' hay tôken LP) nhất định trong [tỷ xích](https://resources.curve.fi/base-features/understanding-gauges) của Curve. Lượng CRV thưởng có thể tăng thêm khi người dùng 'khóa, cất' đồng CRV của mình vào [Két](https://dao.curve.fi/locker). Két này trả lại (cho người vừa 'khóa, cất' CRV) tôken có tên veCRV: Nó cấp quyền biểu quyết quản trị và hưởng một phần thu nhập (lượng phí phải trả khi sử dụng) của giao thức này.

Khóa CRV giúp người dùng 'kích' thưởng đồng CRV sẽ nhận khi cấp thanh khoản vào những bể góp vốn hợp lệ (do quản trị quyết). Hệ số 'kích' được xác định bởi lượng CRV đã khóa và tương quan của chúng trong cả bể góp vốn.

![](https://i.imgur.com/QaMMdr7.png)

Yearn, với việc tạo yVault có tên 'Backscratcher' (tạm dịch: 'Gãi lưng', hàm ý về sự hợp tác tốt cho cả hai), khóa gần như vô thời hạn một lượng lớn đồng CRV. Từ các hệ số kích CRV nhận được, Yearn lại dùng chúng để tăng thêm lợi tức cho hàng loạt yVault khác của mình.

### yVault 'Gãi lưng'

yVault 'Gãi lưng' tận dụng kế hoạch khai thác thanh khoản (liquidity mining) làm vốn theo cách có lợi cho cả Curve và Yearn. 

Người dùng ký gửi đồng CRV vào yVault nói trên để khóa vĩnh viễn số CRV đó. Đổi lại, họ nhận được tôken đại diện cho phần tương ứng của bể góp vốn 'Gãi lưng'. Doanh thu từ Curve (qua chính sách chia sẻ phí Curve) được phân phát vào bể góp vốn 'Gãi lưng', và người ký gửi có thể lấy nó về hàng tuần.

Chưa kể, 10% tất cả đồng CRV do Yearn Finance kiếm được sẽ ký gửi tiếp (gần như) vô thời hạn vào kho 'Gãi lưng'. Bởi vậy, những ai muốn 'đặt cọc' CRV sẽ luôn luôn nhận phần lãi lớn hơn từ doanh thu của yVault 'Gãi lưng' so với việc trực tiếp sử dụng Curve. Họ cũng có khả năng thu được những tôken giá trị khác như SUSHI và PICKLE từ việc cung cấp thanh khoản.

![](https://i.imgur.com/UfCikwk.png)

Người dùng không bao giờ có thể rút lại số CRV ban đầu ký gửi. Nhưng, nhờ sự trợ cấp cho thanh khoản yveCRV và giá trị mà tôken này tích lũy từ hàng loạt nguồn doanh thu, người dùng có khả năng đổi nó lấy một tài sản khác với tỷ lệ nhất định.

Đổi lại, các hệ số kích của lượng CRV bị khóa sẽ về tay Yearn. Chiến thuật như cũ, Yearn tận dụng chúng cho các yVault.

## Tự động hóa lãi kép 

Để tạo lãi kép, người dùng phải trả phí giao tác trên chuỗi khối (blockchain) Ethereum. Phí này dao động tùy theo cung–cầu, có thể trở nên đắt đỏ và làm giảm lợi tức.

Vì yVault gộp chung giao tác của bạn với rất nhiều người khác, chi phí lũy tích trở nên thấp hơn, đồng nghĩa với lợi tức cao hơn khi sử dụng các Vault (Kho bạc). Hiện giờ, phí gas do mạng Keep3r trả hết, nghĩa là người dùng hưởng lãi kép mà không tốn đồng nào.

## Đòn bẩy tài chính 

Yearn hưởng lợi nhờ 'Iron Bank' (C.R.E.A.M. Finance) nhằm tiếp cận với tín dụng để tăng thêm lợi tức cho yVault. Chỉ những địa chỉ mã-thuật-số 'an toàn' (như của Yearn) mới dùng được tính năng này, nghĩa là một cá nhân bình thường không thể tự làm điều đó.

Một số chiến lược còn triển khai chức năng [vay–trả giây lát](https://docs.yearn.finance/resources/defi-glossary#flash-loan) ('flash loan'), vốn là một hệ thống mặt-sau ('back-end') đòi hỏi phải có kinh nghiệm lập trình mới tận dụng được.

## Quan hệ đối tác

yVault 'Gãi lưng' có một không hai, tồn tại được là nhờ sự ăn khớp chặt chẽ với các giao thức như Curve, SushiSwap và Pickle Finance. Quan hệ khắp DeFi (thế giới Tài chính Phi-tập-trung) của chúng tôi giúp những người ký gửi vào yVault có lợi thế lớn, không thể thấy được ở nơi nào khác.

Yearn tích cực hợp tác phát triển với những giao thức giống như trên để tạo ra cơ hội thu lãi mới, đồng thời giúp DeFi trở thành ngành công nghiệp lớn mạnh hơn nữa.
