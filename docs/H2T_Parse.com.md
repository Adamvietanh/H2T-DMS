## Tài liệu mô tả Parse
Tài liệu này giới thiệu về dịch vụ bên thứ 3([Parse](https://Parse.com/)) mà nhóm H2TFC sử dụng để phát triển ứng dụng quản lý phân phối điểm bán hàng.

I. Các thành phần của [Parse](https://Parse.com/) hỗ trợ cho việc phát triển
----------------------------------------------------------------------------
[Parse](https://Parse.com/) gồm 3 thành phần dùng để hỗ trợ cho việc phát triển ứng dụng(không cần phải quan tâm về việc bảo trì server hay kiến thức chuyên sâu về server)
 1. [Parse Core](https://parse.com/products/core) 
 
 	> Là thành phần đóng vai trò quan trọng, được xem như là cơ sở dữ liệu để các client từ phía ứng dụng có thể truy xuất và lưu trữ dữ liệu lên mà không cần phải có server, ngoài ra core còn cung cấp giao diện dashboard trực quan qua giao diện web giúp người dùng dễ dàng thao tác các chức năng mà Parse mang lại.
 2. [Parse Push](https://parse.com/products/push)
 
	> Dùng để gửi đi những tin nhắn, thông báo từ máy chủ Parse.com tới các máy con một cách dễ dàng.
 3. [Parse Analytics](https://parse.com/products/analytics)
 
	> Dùng để theo dõi các thông số hoạt động của ứng dụng tới server.

 II. Chi tiết giá cả của từng thành phần ở Parse
 -----------------------------------------------
 
 Link tham khảo: https://parse.com/plans
 
 Bảng giá cả của các thành phần tại parse.com/plans (cập nhật ngày 16/04/2015)
 ![parse_plan](https://cloud.githubusercontent.com/assets/11812919/7176009/b3e20578-e444-11e4-8670-7cc46488ef29.png)
 1) Parse Core
 
 >	* Parse.com là phần mềm bên thứ 3 cho phép sử dụng miễn phí và có khả năng tăng thêm dung lượng và số lượng truy cập bằng các đóng phí.
 >	* Tuy số lượng truy cập được ghi trên trang chủ của Parse.com là số lượng truy cập/s nhưng thật ra Parse.com tính số lượng truy cập/phút.
 >	> Nên ở đây khi sử dụng miễn phí nên 30 lượt truy cập/s = 1.800 lượt truy cập/phút.Ví dụ khi có 1.000 lượt truy cập cùng lúc vào máy chủ thì Parse.com vẫn có thể xử lý được nhưng trong 1s đó mà có 2.000 lượt truy cập thì sẽ có 200 lượt truy cập sẽ bị từ chối do khi sử dụng hạn mức miễn phí thì Parse.com chỉ chấp nhận 1.800 truy cập/phút.
 >	* Mức phí tối thiểu thành cho Parse Core:
 
 ![111](https://cloud.githubusercontent.com/assets/11812919/7176506/4276cd7e-e449-11e4-8c99-4b9e008192f1.png)

 >	* Mức phí tối đa cho Parse Core:
 
 ![parse_core_max](https://cloud.githubusercontent.com/assets/11812919/7176594/d178f8bc-e449-11e4-97f8-a43a6f2af7d1.png)
 
 Nếu số lượng request mà vượt qua quá số lượng tối đa mà gói dịch vụ Parse có thể cung cấp thì khách hàng có thể trao đổi với nhân viên bên phía Parse để được tư vấn và giải quyết về vấn đề số lượng truy cập này.
 
 Tuy nhiên xin hãy lưu ý cho: 600 lượt truy cập/s là 1 con số rất lớn(36.000 lượt truy cập/phút) kèm với khả năng để tất cả nhân viên cùng làm tại một thời điểm là rất khó xảy ra.

 2) Parse Push
>	* Cũng như Parse Core thì Parse Push cũng sử dụng miễn phí và có khả năng tăng thêm khả năng sử dụng bằng các đóng phí.
>	* Ở hạn mức dùng miễn phí thì Parse Push có khả năng gửi thông báo từ máy chủ xuống các máy con với số lượng giới hạn là 1.000.000 máy con sử dụng ứng dụng truy cập tới Parse.com.
>	* Mức phí tối thiểu cho Parse Push:

![push__min_price](https://cloud.githubusercontent.com/assets/11812919/7176559/922960ca-e449-11e4-924f-59d4ed3407a1.png)

>       * Mức phí tối đa cho Parse Push:

![parse_push_max](https://cloud.githubusercontent.com/assets/11812919/7176595/d17ad466-e449-11e4-85f4-03ecb145cb7c.png)

 3) Parse Analytics
	* Được sử dụng miễn phí hoàn toàn, tuy nhiên do chưa có nhu cầu sử dụng nên nhóm vẫn chưa thêm chức năng này vào sản phẩm.

III. Cách thức hoạt động của Parse trong ứng dụng
-------------------------------------------------
Nhóm phát triển coi việc sử dụng Parse như là 1 cơ sở dữ liệu trực tuyến nên mọi hoạt động truy xuất, gửi dữ liệu đều thông qua Parse để thực hiện. Bên cạnh đó, Parse cũng cung cấp bộ Android SDK hỗ trợ cho việc phát triển ứng dụng trên android nhanh hơn cho nhóm.

Để kết nói ứng dụng với Parse Core, Parse sẽ cung cấp cho người dùng các API Key để xác thực, do đó nên nếu các ứng dụng muốn sử dụng chung 1 cơ sở dữ liệu thì sẽ dùng chung 1 API Key và ngược lại nếu muốn các cơ sở dữ liệu khác nhau để cung cấp cho từng khách hàng thì chỉ cần dùng các API key khác nhau.

Coi hướng dẫn cách cài đặt Parse tại đây: [hướng dẫn cài đặt](https://github.com/BuiThienDuy/H2T-DMS/blob/master/docs/H2T_DMS_Huong_dan_cai_dat.md)

Tham khảo thêm cách sử dụng Parse trong android tại đây(dành cho developer): https://parse.com/docs/android_guide

 
IV. Câu hỏi thường gặp
----------------------
Câu hỏi 1: cách thức truyền và tải dữ liệu giữa Parse và các máy con như thế nào?
	
Trả lời: Parse sử dụng Parse REST API để gửi dữ liệu xuống máy con với gói dữ liệu JSON qua giao thức HTTPS. Dưới sử hỗ trợ của Parse Android SDK, gói dữ liệu JSON sẽ được chuyển qua dạng ParseObject để sử dụng dễ dàng trong việc phát triển hơn.

Câu hỏi 2: Parse sử dụng loại cơ sở dữ liệu nào cho android
	
Trả lời: Parse sử dụng [MongoDB](https://www.mongodb.org/) để làm cơ sở dữ liệu cho android thuộc kiểu cơ sở dữ liệu NoSQL.

	
