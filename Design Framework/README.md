# Design Framework
## Cmake:
Là một trong những công cụ khá quen thuộc và phổ biến cho những LTV thiết bị nhúng. Có chức năng là sinh ra Makefile hiệu quả. 

Ứng dụng này có mục đích làm giảm dung lượng các file chia sẻ trên mạng bằng cách tạo ra các file config cần thiết cho project, khi đó người chia sẻ source và người sử dụng chỉ cần chia sẻ những file code. Cmake hỗ trợ rất nhiều project của nhiều ngôn ngữ khác nhau, nhiều phiên bản của các IDE nổi tiếng và nhiều option để người dùng lựa chọn.

Lấy 1 thí dụ về project C++ chạy bằng Visual studio: Project cần các file như ***.sln, *.vcxproj, vcxproj.filters,… chứa thông tin về project, như là project đó cần compile những file nào, solution có bao nhiêu project, project build trên platform nào,…** thì Cmake sẽ tạo ra các file đó giùm bạn.

Còn nếu không có Cmake thì sao? Người chia sẻ file sẽ phải tạo ra các file config ứng với mỗi phiên bản IDE, chỉ riêng Visual Studio đã có nhiều phiên bản: VS 2008, VS 2010, VS 2012, VS 2013, VS 2015, VS 2017. Cộng thêm các ngôn ngữ khác nữa thì số lượng file phải tạo ra quá nhiều. Làm cho dung lượng file chia sẻ tăng lên đáng kể.

Cmake thuận tiện cho tất cả các framework trong C/C++ 

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

   ![](./images/demo.PNG)
   
   _Một hình ảnh sau khi đã build các file cấu hình cho IDE bằng Cmake_
   
_VD0: [Hello world với C trong Cmake](./Example/VD0.md)_



_VD1: Viết chương trình mô phỏng máy tính bỏ túi với các file header (sum.h, sub.h, multiple.h, divide.h)_

_VD2: Ứng dụng quản lý sinh viên với việc sử dụng các file header **(sort.h, search_student.h, update_info.h)** với việc build static library và dynamic library_

_VD4: Opencv với Cmake_

- Step 1: Download [OpenCV](https://github.com/opencv/opencv) and [Cmake](https://cmake.org/)
- Step 2: Build opencv with cmake
  
  ![](https://lh3.googleusercontent.com/h1KeRk2TvnC6QahnDYdfIPLje9rG8K7HNNFDPup9w-qrIeWHQdmgsBtgXegJhKbvBS0KMZ0TmAbtTkGpsVXVqhqByeZBKJoweNrSFwCPh0QUnNDNnsu-DU0F7yW1BdOHm71rN3BAIYGSXtAQzBP7rFU-Of18n2ktuY2yFEuh374bOYQR24w7gMZKSpXNZQgGDJovxVK4pl3Cwy9DqYu76ZdgYZmDkZYYLAJFKUmNBNKw-qmAHR2-KAnNuuhz_BOZyPuTxTdD9M7M7kG6daEjE77BdxAxJVdf7PIfo5qYPyqq26i2iZ9HzJXdqN-q0sdyC5jU2nj7lnSf0WTRGRSrrC0OArg2flsIGL7HKnrsDyE4tTKW3hbqiZ8too294tpcdPHO6Os4e01LGlIhhHvjV8u3lg4BJs5Ke86iLK748otHr-kKs-Qi3XmPVSc2trhjfZZQ3j7Rg1N19kWbU6EtROzsfbmx85ykQJCei4lU7kPxuPRld_w_PIMfDfaxUSYl5VQZ0uppIsg7bsHXIXPT-oYoOGyCcaSBWntznPKK0F2F0zchnRKCgH4Ye5f0amxQZtZ9X1mN0uujIb4R1Sc7-jFo-YRpbf8rG7796s2417f-6HBeKFUyVd_zP-3CfbMC6w_Q1FJPDzhTCoNfbAcpeGlZv5RqEN5fNPmLU38-MWUw6EDpsjzEyonIXGZ-ZVjOWe6fOUs2UJMA9G-SZA=w925-h177-no)
  
  + Press **configure**, choose **visual studio 2015**, finish
  + Then press **generate**
- Step 3:
  
  Open **OpenCV.sln** under **build/**
- Step 4: Build it using **Debug, Release**

  ![](https://lh3.googleusercontent.com/V1vZJwO-fTGwrqzt9kiCZKsMl3wQvvVpsK5Mkqwh-DbhUDqcxCQj7RVrbdFh4OfYPQbkYfF6O6bTuRBRF4y0OlaCBztwJ0Of2KdcoYtMB45CFBvaaLXFjjo2TDinqgeALNcL0IKbwqZR0vKxDjow58F-OhnImyQ_xwp8E4OXSvaqQGYgDL0OR8VjxS_e8YpjnkvlHSC-Co6CLvUcklnuEV03hRBV_G7mhnPxLK0NacPcHVMYn35sSBG1TRJOhsVU3HUs33y2VX1eM058z1V4Dd_Vt0Hic8bxwajVMokMZ6hK0h1WfQasoddtK9z3k4QNSoBOfsA9RKKm7N7VH0ygvGsj5vWZZBURgSLLJparmSvYXsKZXqkh1dwLb11NbiaLnvqnsGnsT2fpx9vNssatg6_Z3Ju4y3DJZpKoX9PM5AaS1kuj3y0NxmarkuRY8ES_N3ASq7rgzeFTlECcAtRBtXZGDtyJu4o6RfnUseF2wETC9x596EDCyxFXYOR4THnwautqsOE8uV4DmTU15Pjk-v7wfE1vCVLsyN0oAWf-nbt9VaoFwh3yFuXAnIEgt7JyephRVPmLgeXejyh3CHdpZcdjbXCVA0ZCo4Zar20YiDtL8P_Wjzqdeiq_T0TYxzVQDq6_1OEwhuqybah47VeOtmvtnIuZIpTnVp_vKaaZkQhKV3ZI_MWWEyNwsPaovl1DA0ugxElAfEmgZZ-F_A=w347-h186-no)
  
  * Right **click > build**
  * Switch to **Release** mode and build again
- Setting up **environment variable**
  - add `<opencv>/bin into PATH` 
  
  ![](https://lh3.googleusercontent.com/DOIjfM1uhVJc_WelsnebvsoC-niX918kg7nApD8sUa9DYy1DMoP8Zmz77BtRd0rWqR3TFFjIWgLJYJTiA0qvsrVRloA0rJL4fCdO5PAJdyk4rNLZr3wPq-Zv-lK9rMwIFRgLqng-D-I-m3udOkrB-Zt-3oNt6jseOeBN8F2NYSsVDmVOK1f5ZAlnEToz0x_iniDBOfLE3ivG348g_6arZlwExNJxri5g_jIkhDeIXhE1m8ycLyyxVijobnrrZi7pKRkz5nDSO6Rnxx84q9_IkqKjlEg5fk0_GJm3kcRPgOLgF2WAkld2FhdfPnDfJvyphZpJBbJ2nfrVCjXhDjl7ugdAG-wjvVdF6fJK1LpBvAgto-7d5G3-n7f4t10mYu6FPrk7pDND0dy0xBwxcsz71U-_DNam9ItD38MfjbuQa5brGM0hQ_be5gaCqRMVuhcRF67GpiDCV-GeabGsmGIHRWIVAxjupJkDhZu-NlqwH71onLO7jOas5noWX8tV-vN_B21o-7uL1sDKZiew4hGt3KhV_bq38utCvJnjHf7JMoQ8fnYSNxS7BKZF9zLrOvWr3mKD7JI6OqsH1--R9v3uHAyF1kgYnF7cH-VQWRpXhX3NCn9BeWRVwi496QHPgVQ4C7HM8FtuxvKRBRNWq7p07f7f9liX3qjsI09Pb0h4pftWyqodMJ1giczZ7P7y04o0ZCMKNhETnvT9DVvqYw=w733-h547-no)
  
  - Add new environment named **OpenCV_DIR**, value as `<opencv>/build`
  - It may need logout to apply setting, you can check it by **echo %PATH%, echo %OpenCV_DIR%**





