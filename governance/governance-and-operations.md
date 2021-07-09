# Quản trị và Hoạt động

Sau khi [YIP-61: Quản trị 2.0](https://gov.yearn.finance/t/yip-61-governance-2-0/10460) được duyệt qua vào ngày 25/04/2021, Yearn bắt đầu quá trình chuyển giao sang cấu trúc **đa-ĐAO**, một mô hình quản lý bằng việc **ủy quyền có hạn chế**. Cách tiếp cận này cho phép phát triển giao thức theo cách linh hoạt hơn, ít quan liêu mà vẫn giữ được mức độ phi-tập-trung xác đáng. 

Đa-ĐAO là tập hợp một số lượng linh hoạt nhiều ĐAO (viết tắt của "Decentralized Autonomous Organization", tạm dịch: Tổ chức Tự trị Phi-tập-trung) cùng đóng góp cho giao thức theo cách riêng. Các nhóm độc lập này bao gồm những người giữ đồng YFI ('chủ YFI'), các yTeam và Ví đa-ký (hay Ví chung, "Multisig").

- **Chủ YFI** biểu quyết các thay đổi của giao thức hoặc cấu trúc quản trị giao thức
- **Các yTeam** tập trung vào khía cạnh cụ thể của giao thức hoặc hoạt động liên quan
- **Ví đa-ký** là tập hợp những thành viên có quyền thực hiện hoặc bác bỏ bất cứ quyết định trực-chuỗi ("on-chain") nào

Những người nắm giữ Tôken có tiếng nói tối cao trong việc quyết định yTeam nào tồn tại, ai được phép vào Ví đa-ký, cũng như giới hạn quyền kiểm soát hoạt động của mỗi nhóm. Cụm từ 'ủy quyền có hạn chế' bắt nguồn từ việc chủ tôken giao phó một số quyền cụ thể cho nhiều nhóm khác nhau để cùng xây dựng và quản lý Yearn.

Nói một cách đơn giản, quá trình quản trị diễn ra như sau:

    1. Chủ YFI khởi tạo, hủy bỏ hoặc xác định giới hạn cho các yTeam
    2. yTeam thông báo cho yTx về một quyết định
    3. yTx tạo một giao tác ủy quyền và gửi đến Ví đa-ký
    4. Ví đa-ký thực hiện hoặc bác bỏ giao tác đó
    
## Trách nhiệm của ĐAO

![](https://i.imgur.com/aqrm7le.png)

### Chủ sở hữu Tôken 

Những người nắm giữ [đồng YFI](https://docs.yearn.finance/governance/yfi) có trách nhiệm tạo và biểu quyết các đề xuất nhằm cải thiện giao thức này.

| Đề xuất | Mô tả |
|-----------|--------------|
|Đề xuất Cải thiện Yearn (YIP)|Một đề xuất để thực hiện dựa theo bất cứ quyền nào mà chủ đồng YFI có, hay thậm chí cả những quyền bên ngoài phạm vi được liệt kê|
|Đề xuất Ủy quyền Yearn (YDP)|Một đề xuất để thay đổi nơi ủy thác bất cứ quyền quyết định riêng nào|
|Đề xuất Thăm dò Yearn (YSP)|Một đề xuất không-bắt-buộc phải thực hiện, nhằm thăm dò ý kiến của cộng đồng hoặc ra hiệu phương án giải quyết bất cứ vấn đề nào|

Cụ thể, các đề xuất trên cho phép chủ tôken ra những quyết định sau:

| Quyền | Mô tả |
|-------|-------------|
|Quản lý mọi Quyền|Chủ đồng YFI có thể biểu quyết để tạo, phân công những quyền riêng cho một hoặc nhiều yTeam, cũng như thu hồi chúng|
|Thay đổi Hợp đồng Tôken YFI|Bất cứ giao tác nào liên quan đến hợp đồng của tôken YFI, chẳng hạn như tạo thêm hay đốt bỏ các "chìa tạo" ('minting key') đồng này, đều do những người nắm giữ tôken YFI kiểm soát|
|Áp Phí|Áp đặt cấu trúc phí cơ bản cho Giao thức Yearn|
|Thay đổi Người ký Ví chung (Multisig)|Do Ví chung (Multisig) tiếp tục sở hữu nhiều quyền tối quan trọng trong thời gian chuyển giao, các chủ sở hữu đồng YFI là bên duy nhất có thể biểu quyết để thay đổi những thành viên ký ví này|
|Phê chuẩn yTeam|Chính thức thành lập hoặc giải tán các yTeam để kiểm soát yTeam nào có thể giữ quyền được ủy thác|
|Thay đổi Người ký yOps|Đây là một quyền đặc biệt để quản lý yOps, do yOps có khả năng thay đổi người ký của những yTeam khác|
|Sử dụng Ngân quỹ|Dùng ngân quỹ để chi tiêu|
|Quyền YIP|Chủ đồng YFI có quyền đề xuất một YIP về bất cứ điều gì chưa ủy thác hay đề cập|
### yTeam

Mỗi yTeam có mục tiêu và quyền riêng, được ấn định bởi những người nắm giữ tôken. yTeam hình thành từ hội thành viên, vốn là các nhóm cộng tác độc lập, cùng làm việc hướng đến mục đích tương tự như ê-kíp lớn. Thêm vào đó, một hội thành viên có thể thuộc về nhiều yTeam.

| yTeam | Mục tiêu | Hội Thành viên (tên chính thức và tạm Việt hóa) |
|-------|-----------|-----------------|
|yGuard|Bảo vệ các Vault (Kho bạc)|YFI Protocol Dev (Hội Lập trình), YFI Strategists (Hội Chiến lược gia), YFI Mechanics (Hội Thợ máy), YFI Secret Admirers (Hội Mê Kín)|
|yBrain|Quản lý các chiến lược|YFI Strategists (Hội Chiến lược gia)|
|yDev|Quản lý giao thức|YFI Protocol Dev (Hội Lập trình)|
|yPeople|Phụ trách giám tuyển ê-kíp|YFI Compensation Working Group (Nhóm Đãi ngộ Công tác), YFI Advisors (Hội Cố vấn)|
|yBudget|Sử dụng tiền hiệu quả|YFI Finances (Hội Tài chính), YFI Advisors (Hội Cố vấn)|
|yFarm|Gia tăng ngân quỹ|YFI Secret Admirers (Hội Mê Kín), YFI Secret Entrance (Hội Đường Mật)|
|yTx|Ghi giao tác hoặc giao dịch|YFI Doers (Hội Chấp hành)|
|yOps|Phối hợp các cộng tác viên|YFI Ops (Hội Vận hành)|

Mỗi yTeam được giao một số quyền cụ thể, được ấn định theo YIP-61: 

| yTeam | Quyền | Mô tả |
|-------|-------|-------------|
|yGuard|Quyền Khẩn cấp|Ngay lập tức can thiệp trong trường hợp bị tấn công hoặc xảy ra lỗi, có thể dừng hẳn hay khôi phục chiến lược cũng như các Vault (Kho bạc)|
|yBrain|Quản lý Chiến lược|Kích hoạt, tạm dừng, tinh chỉnh và bảo trì các chiến lược|
|yDev|Xác định Giao thức Yearn|Quyết định mã lập trình nào là một phần của Yearn|
|yDev|Quản lý Giao thức|Duy trì và cải thiện Giao thức Yearn|
|yDev|Bổ sung Chiến lược|Thêm nhiều chiến lược mới cho các Vault (Kho bạc)|
|yTx|Ủy thác Giao tác|Tạo các giao tác hoặc giao dịch cho Ví chung (Multisig) để ký và thực hiện|
|yPeople|Thưởng các Ê-kíp|Tạo, triển khai, điều chỉnh hoặc chấm dứt các gói đãi ngộ của Yearn|
|yBudget|Thiết lập Ngân sách|Tạo ngân sách cho Coordinape (một giải pháp cộng tác liên dự án), trợ cấp, tuyển dụng, hoạt động hoặc các luồng công việc khác|
|yFarm|"Cày" tiền bằng Ngân quỹ|Vận dụng, đầu tư và thu lời với ngân quỹ nhàn rỗi, cũng như ra quyết định về các Airdrop|
|yOps|Phê chuẩn Người ký yTeam|Chính thức chấp nhận hoặc loại bỏ những người ký giao tác cho mỗi yTeam|

### Ví chung (Multisig)

Các quyết định của yTeam sẽ được Ví chung (Multisig) thực hiện trực-chuỗi (on-chain) cho tới khi một hệ thống phi-tập-trung tốt hơn hoàn thiện và ra mắt. Trong lúc đó, [Ví chung (Multisig)](https://docs.yearn.finance/resources/faq#who-is-on-the-multisig) kiểm soát những điều sau:


| Quyền | Mô tả |
|-------|-------------|
|Quyền Thực hiện|Quyền chấp hành, hiện thực hóa những quyết định của chủ đồng YFI và các yTeams một cách trực-chuỗi (on-chain)|
|Quyền Bác bỏ|Cho phép Ví chung (Multisig) bác bỏ bất cứ quyết định nào, nhưng quyền này không cần sử dụng trong điều kiện lý tưởng hiện tại|
|Quyền Chuyển giao|Quyền tạm thời cho phép Ví chung (Multisig) hoạt động theo chỉ thị của YIP-41 cho đến khi một bộ các quyền quyết định bao hàm hết mọi giao tác cần thiết|


## Kế hoạch Tương lai 

Yearn không ngừng tìm cách hướng đến mức cân bằng lý tưởng giữa sự phi-tập-trung và hiệu quả hoạt động của ĐAO. Hiện tại, những nỗ lực cải thiện vẫn phần lớn ở bề nổi về mặt xã hội/cộng đồng. Trong tương lai, chúng tôi sẽ tiến tới việc thực hiện bằng mã lập trình và phần mềm, chẳng hạn như: 

- Cơ chế đồng thuận Đa-ký (Multisig), cho phép từng yTeam sở hữu Quyền Thực hiện 
- Chuyển từ biểu quyết ở lớp trung gian (proxy) sang biểu quyết trực-chuỗi (on-chain)
- "Tôken hóa" các quyền quyết định thành NFT ("Non-Fungible Token"—một dạng Tôken độc đáo, không cái nào giống cái nào)
- Tận dụng [Coordinape](https://coordinape.com/) cho những việc như phân bổ ngân sách và đãi ngộ
