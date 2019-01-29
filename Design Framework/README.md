# Design-Framework-for-Complex-Project-C-plus-plus

## Toolchain:

## Cross compiler:

## Cmake:
Là một trong những công cụ khá quen thuộc và phổ biến cho những LTV thiết bị nhúng. Có chức năng là sinh ra Makefile hiệu quả. 

Ứng dụng này có mục đích làm giảm dung lượng các file chia sẻ trên mạng bằng cách tạo ra các file config cần thiết cho project, khi đó người chia sẻ source và người sử dụng chỉ cần chia sẻ những file code. Cmake hỗ trợ rất nhiều project của nhiều ngôn ngữ khác nhau, nhiều phiên bản của các IDE nổi tiếng và nhiều option để người dùng lựa chọn.

Lấy 1 thí dụ về project C++ chạy bằng Visual studio: Project cần các file như ***.sln, *.vcxproj, vcxproj.filters,… chứa thông tin về project, như là project đó cần compile những file nào, solution có bao nhiêu project, project build trên platform nào,…** thì Cmake sẽ tạo ra các file đó giùm bạn.

Còn nếu không có Cmake thì sao? Người chia sẻ file sẽ phải tạo ra các file config ứng với mỗi phiên bản IDE, chỉ riêng Visual Studio đã có nhiều phiên bản: VS 2008, VS 2010, VS 2012, VS 2013, VS 2015, VS 2017. Cộng thêm các ngôn ngữ khác nữa thì số lượng file phải tạo ra quá nhiều. Làm cho dung lượng file chia sẻ tăng lên đáng kể.

+ Cài đặt Cmake trên Windows: Tải và cài đặt [ở đây](https://cmake.org/download/)
+ Cài đặt Cmake trên Linux: 

  ```
  wget https://cmake.org/files/v3.12/cmake-3.12.0.tar.gz
  tar xzf cmake-3.12.0.tar.gz
  cd cmake-3.12.0
  ./configure --help
  ./configure --prefix=/opt/cmake
  make 
  make install 
  ```

  **Verify installed:** `/opt/cmake/bin/cmake -version` 

   ![](https://github.com/BreakthroughCode/Design-Framework-for-Complex-Project-C-plus-plus/blob/master/images/demo.PNG)
   
   _Một hình ảnh sau khi đã build các file cấu hình cho IDE bằng Cmake_
   
_VD0: [Hello world với C trong Cmake](https://github.com/BreakthroughCode/Design-Framework-for-Complex-Project-C-plus-plus/blob/master/Example/VD0.md)_



_VD1: Viết chương trình mô phỏng máy tính bỏ túi với các file header (sum.h, sub.h, multiple.h, divide.h)_

_VD2: Ứng dụng quản lý sinh viên với việc sử dụng các file header **(sort.h, search_student.h, update_info.h)** với việc build static library và dynamic library_

_VD4: Opencv với Cmake_

## Contributor:

_Hau Trung Nguyen_

_haunt.hcm2015@gmail.com - haunt.hcm2015@outlook.com_
