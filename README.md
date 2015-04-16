![ic_launcher](https://cloud.githubusercontent.com/assets/11812919/7166809/6e1fb004-e3da-11e4-9f92-83c4587eb777.png)
H2T DMS
=============

**H2T DMS** là một ứng dụng cho android sử dụng API của [Parse](https://parse.com/) cho việc quản lý điểm phân phối bán hàng.

## Tổng quan hệ thống
Dựa trên yêu cầu nhóm xác định ra có 2 vai trò chính trong ứng dụng này là: nhân viên kinh doanh và nhân viên quản lý(vùng,khu vực, giám đốc kinh doanh) được định nghĩa như trong hình dưới đây:
![tong_quan](https://cloud.githubusercontent.com/assets/11812919/7176035/edb525f0-e444-11e4-9c1c-b9b91a57e737.png)


Dưới tính đặc thù của dự án nên nhóm quyết định thiết kế sản phẩm H2T DMS theo hướng chia sản phẩm ra làm 2 phần chính để phát triển gồm:
 1. [H2T_DMS_MANAGER](https://github.com/BuiThienDuy/H2T_DMS_MANAGER/): ứng dụng dành cho nhân viên quản lý
 2. [H2T_DMS_EMPLOYEE](https://github.com/BuiThienDuy/H2T_DMS_EMPLOYEE/): ứng dụng dành cho nhân viên kinh doanh.

Ngoài ra ứng dụng cần được xây dựng theo mô hình client-server để đáp ứng cho việc sử dụng chung một cơ sở dữ liệu của nhân viên kinh doanh và nhân viên quản lý.

## Kiến trúc
Dưới thời gian gấp rút của dự án và nhóm hiện không có nhân lực có kinh nghiệm về backend server nên việc thiết kế và phát triển backend server của nhóm bị loại ra và ưu tiên cho việc hoàn thành sản phẩm đầy đủ chức năng và đúng thời gian được đặt ra.


Phương án thay thế cho việc không phát triển server của nhóm là: sử dụng dịch vụ bên thứ 3 có tên là [Parse](https://parse.com/) để làm backend server.

Nhóm cũng đã tài liệu lại mô tả về dịch vụ bên thứ 3 có thể đọc qua: [link](https://github.com/BuiThienDuy/H2T-DMS/blob/master/docs/H2T_Parse.com.md)

## Các bản release/demo sản phẩm
* H2T_DMS_MANAGER:  https://github.com/BuiThienDuy/H2T_DMS_MANAGER/releases
* H2T_DMS_EMPLOYEE: https://github.com/BuiThienDuy/H2T_DMS_EMPLOYEE/releases

## Thông tin nhóm phát triển và mentor
* **Nhóm H2TFC gồm:**
 	* Bùi Thiện Duy
	* Nguyễn Hà Nhật Năng
	* Phạm Thành Dương
	* Lai Thanh Phuong
	* Lương Yến Nhi
	* Lê Nguyễn Thanh Thanh
* **Mentor:** Trần công Thanh

## Liên hệ hỗ trợ
Nếu có bất kỳ thắc mắc gì liên quan đến dự án, vui lòng gửi email tới địa chỉ thanhduongpham4293@gmail.com để được hỗ trợ.

----
