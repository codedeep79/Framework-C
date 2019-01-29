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

### Build with EXTRA MODULES
- In step 2 above. build `opencv` with `cmake`, press **configure**
- Set up **OPENCV_EXTRA_MODULES_PATH** to proper path(<[opencv_contrib](https://github.com/opencv/opencv_contrib)>/modules) 
   
  ![](https://lh3.googleusercontent.com/F7qfChAVqYqpT4e4TWiVlxpZ-JH7rPXFaaqOb9K6xWMa8sma15h1t82rI-E2bwFVgGq1178Ijwg6d1PwOBVbIijOzLtPOGJC9zcf98dehOMpWZn-PyowjaP8nIIioAC4jryhYsAr3lP5A0m_qs2DcHCgS9Hd3rlD6Z-CxuSmMPg8yg9tf_uvZ-uhQ9W5MH4nbEUJE6MdKgJGaR8taEDBqQaG35TPEwmol9DYElWlqnrFZ2BX7EIxiVcW7Tv96-7m9hRIg9jfL8-cKGhG1F_Yble1dLRXyRPQQIWgQQH7-W4JjNJu5f7YFnZB5ZNoceE5mlW_PjRgSi2-lXDjgDc4Pee3XzyULcYvDEaXUiypBSDveKm6n9lwJeQP-UHO9ce4j9C0a7F0CfAAcFnlmEPc9c7u-lAIX3XQVNv7UAiXfEVePp1_FdH2BzLNvbDUBqzPQ1UpegI5WuoUPLrYTBA3-M0VED-V1jgd9jca3rg7rsxJKj6-HxLzT30I2WRo-aoBugLFek6jHNyKcl8uGhxbO4Oi8w0IZ6Fq4n7d4g-DTrO-L0PMyLh4etvKdk_naYb_L3mdGRYFDSLsIg4g10ajJ81IieTJYOwxKqyhI1zlCrBY2EsqgzbL3btn8cYYWmzsPXHlxjq85RHhzOGRYi-UpR8ovVEi-6-usd_G9huR-R0FSnLhzYqoa1TyF9MR8ApjDypgQ64JSX8oHPskVQ=w923-h236-no)
  
- Press **configure** again, then **generate**

- Test CI: Sign in and sync your Github account at https://travis-ci.org

  Travis.yml example:
  
  ```yml
  language:
    - cpp

  compiler:
    - gcc

  before_install:
    - sudo apt-get update

  install:
    # OpenCV dependencies - Details available at: http://docs.opencv.org/trunk/doc/tutorials/introduction/linux_install/linux_install.html
    - sudo apt-get install -y build-essential
    - sudo apt-get install -y cmake git libgtk2.0-dev pkg-config libavcodec-dev libavformat-dev libswscale-dev
    - sudo apt-get install -y python-dev python-numpy libtbb2 libtbb-dev libjpeg-dev libpng-dev libtiff-dev libjasper-dev libdc1394-22-dev

    # Download v3.1.0 .zip file and extract.
    - curl -sL https://github.com/Itseez/opencv/archive/3.1.0.zip > opencv.zip
    - unzip opencv.zip

    # Download EXTRA MODULES and extract.
    - curl -sL https://github.com/Itseez/opencv_contrib/archive/3.1.0.zip > opencv_contrib.zip
    - unzip opencv_contrib.zip

    # Create a new 'build' folder.
    - cd opencv-3.1.0
    - mkdir build
    - cd build

    # Set build instructions for Ubuntu distro.
    - cmake -D OPENCV_EXTRA_MODULES_PATH=../../opencv_contrib-3.1.0/modules CMAKE_BUILD_TYPE=RELEASE -D CMAKE_INSTALL_PREFIX=/usr/local -D WITH_TBB=ON -D BUILD_NEW_PYTHON_SUPPORT=ON -D WITH_V4L=ON -D INSTALL_C_EXAMPLES=ON -D INSTALL_PYTHON_EXAMPLES=ON -D BUILD_EXAMPLES=ON -D WITH_QT=ON -D WITH_OPENGL=ON ..

    # Run 'make' with four threads.
    - make -j5

    # Install to OS.
    - sudo make install

    # Add configuration to OpenCV to tell it where the library files are located on the file system (/usr/local/lib)
    - sudo sh -c 'echo "/usr/local/lib" > /etc/ld.so.conf.d/opencv.conf'

    - sudo ldconfig
    - echo "OpenCV installed."

    # We need to return to the repo "root" folder, so we can then 'cd' into the C++ project folder.
    - cd ../../

  script:
    - cmake CMakeLists.txt
    - make
    - ./a.out

  ```


