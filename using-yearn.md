# Sử dụng Yearn       

Nhờ tính năng có tên 'zap', bạn sẽ thấy cực kỳ dễ dàng khi ký gửi vào bất cứ Vault (Kho bạc) nào với hầu hết mọi Tôken.

Cách dùng như sau: 

Đầu tiên, **Kết nối ví của bạn** bằng nút tương ứng ở góc trên bên phải. Nhiều loại ví đều được hỗ trợ, nhưng hầu hết mọi người sử dụng [MetaMask](https://metamask.io/), vốn có thể tải xuống miễn phí dưới dạng tiện ích mở rộng Chrome extension, hoặc từ App Store của Apple và Android. Đồng thời, hãy kết nối ví của bạn đúng với mạng Ethereum chính (Mainnet). 

<p align="center">
  <img width="1266.75" height="345.75" src="https://i.imgur.com/H0Uc8e8.png">
</p>

## Nếu bạn **đã có Tôken cần thiết** cho Vault (Kho bạc) muốn ký gửi rồi: 

1. Chọn Vault (Kho bạc) muốn ký gửi vào.
2. Nhập lượng Tôken để ký gửi vào. Nếu ký gửi đồng ETH, đừng quên chừa lại một chút ETH để trang trải phí gas cho các giao dịch khác khi cần trong tương lai. 

<p align="center">
  <img width="914.26" height="360.75" src="https://i.imgur.com/LGdRAMQ.png">
</p>

3. Click nút 'Duyệt' hoặc 'Ký gửi', nếu trước đó đã duyệt tôken này rồi
4. Ví cá nhân sẽ yêu cầu bạn xác nhận giao dịch. Tác vụ này thường tốn khoảng 3 phút, nhưng có thể nhanh gấp nhiều lần nếu [trả phí gas cao hơn cho mạng](https://blog.leverj.io/how-to-set-the-gas-limit-and-gas-price-in-metamask-1b33c38c32fd). Trong trường hợp giao dịch bị tắc nghẽn, hãy xem [hướng dẫn này](https://metamask.zendesk.com/hc/en-us/articles/360015489251-How-to-Speed-Up-or-Cancel-a-Pending-Transaction) để biết cách tăng tốc hoặc hủy bỏ giao dịch đó.

<p align="center">
  <img width="258.75" height=" 459.75" src="https://i.imgur.com/BkXBANS.png">
</p>

6. Khi giao dịch thành công, bạn sẽ thấy số dư ký gửi tương ứng trên giao diện của Vault (Kho bạc), thường xuất hiện trên đầu danh sách các kho.

<p align="center">
  <img width="928.5" height="93.75" src="https://i.imgur.com/JvNQ3l2.png">
</p>

Khi muốn rút: 

1. Chọn Vault (Kho bạc) muốn rút.
2. Nhập lượng cần rút, hoặc click 'Tối đa' để rút toàn bộ số dư.

<p align="center">
  <img width="910.5" height="361.5" src="https://i.imgur.com/Y3NsCRb.png">
</p>

3. Click 'Rút'
4. Ví cá nhân sẽ yêu cầu bạn xác nhận giao dịch. Xem bước 4 ở trên để biết thêm chi tiết. 
5. Khi giao dịch thành công, số Tôken sẽ xuất hiện trở lại trong ví của bạn

## Nếu bạn **chưa có Tôken cần thiết** cho Vault (Kho bạc) muốn ký gửi vào:

Tình huống này rất thường gặp, bởi các Vault (Kho bạc) ở Yearn tạo lãi bằng cách tận dụng tôken của bên cung cấp thanh khoản ('Liquidity Provider' hay viết tắt là LP) qua ứng dụng [Curve Finance](http://curve.finance/), vốn thu được sau khi ký gửi vào một bể góp vốn của Curve.

Ví dụ, nếu muốn ký gửi vào kho crvSTETH (khác với kho ETH), chấp nhận thêm rủi ro gắn liền với bể góp vốn Curve và một phái sinh của ETH (stETH) để thu về lãi suất cao hơn, nhưng lại chỉ có ETH trong ví cá nhân, ETH của bạn sẽ cần phải quy đổi sang tôken crvSTETH trước khi gửi được vào kho tương ứng. 

Rất may, nhờ tính năng 'zap' của Yearn, tất cả những bước rắc rối trên đều được tính hết vào chỉ một giao dịch lúc ký gửi vào. Dưới đây là hướng dẫn dựa trên kho crvSTETH làm ví dụ:

**CHÚ Ý:** 'Zap' tôken vào một kho sẽ cần nhiều giao tác hơn việc ký gửi tôken chuẩn. Điều này nghĩa là bạn sẽ phải trả nhiều phí gas hơn, cũng như có khả năng mất chút tiền do hiện tượng 'trượt giá' khi tôken được bán đổi hay ký gửi vào bể góp vốn. Yearn hạn chế trượt giá ở mức 1%, tức là giao dịch sẽ thất bại nếu trượt giá cao hơn thế (tránh mất quá nhiều tiền vô ích). Trong trường hợp này, bạn sẽ phải bán đổi hoặc ký gửi tôken một cách thủ công. Hãy xem mục [zap](https://docs.yearn.finance/yearn-finance/yvaults/overview#zap-in-with-any-asset) của chúng tôi để biết thêm chi tiết.

1. Chọn kho crvSTETH
2. Click ô thả-xuống cạnh nút 'Duyệt' hay 'Ký gửi' 
3. Chọn tôken muốn quy đổi thành crvSTETH. Danh sách sẽ chỉ hiện các tôken đang có trong ví của bạn.

<p align="center">
  <img width="909" height="363" src="https://i.imgur.com/6K1luO7.png">
</p>

4. Nhập lượng tôken muốn nạp rồi click 'Duyệt' hoặc 'Ký gửi', nếu trước đó đã duyệt tôken này rồi. 
5. Xác nhận giao dịch ở ví của bạn. Xem bước 4 ở mục phía trên để biết thêm chi tiết. 
6. Khi giao dịch thành công, bạn sẽ thấy số dư ký gửi tương ứng trên giao diện của Vault (Kho bạc), thường xuất hiện trên đầu danh sách các kho.

Khi muốn rút: 

1. Chọn kho crvSTETH
2. Click ô thả-xuống cạnh nút 'Rút'

<p align="center">
  <img width="915.75" height="600.75" src="https://i.imgur.com/2UyXKN0.png">
</p>

3. Chỉ định loại tài sản muốn thu về sau khi rút. Bạn có thể chọn crvSTETH, ETH, BTC, DAI, USDC hoặc USDT
4. Nhập lượng muốn rút, hoặc click 'Tối đa' để rút toàn bộ số dư.
5. Xác nhận duyệt nếu cần, sau đó duyệt giao tác rút.
6. Khi giao dịch thành công, số Tôken tương ứng sẽ xuất hiện trong ví của bạn

## Các công cụ để theo dõi tiền của bạn

Nếu muốn xem thay đổi số dư (thường đo theo đô-la Mỹ USD) khi tài sản của mình đang ký gửi trong một Vault (Kho bạc), hãy kết nối ví cá nhân với [zapper.fi](https://zapper.fi) hoặc bất kỳ ứng dụng theo dõi đầu tư tương tự. Đây cũng là cách đơn giản nhất để xem lượng lợi nhuận đã tích lũy được.

Số dư SẼ KHÔNG tăng liên tục. Lợi nhuận được chia theo phần của bạn trong Vault (Kho bạc) khi hệ thống gọi chức năng harvest(), vốn diễn ra bất thường.

Các nguồn (từ cộng đồng) để giám sát lợi nhuận:

- [Zapper](https://zapper.fi/)
- [Zerion](https://app.zerion.io/)
- [Bộ tính ROI Kho bạc Yearn](https://yearn-roi.xyz/#/)
- [yVault ROI](https://yvault-roi.netlify.app/)
- [https://trackavault.com/](https://trackavault.com/)

