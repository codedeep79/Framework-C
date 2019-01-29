# Framework-C-plus-plus
## Install some library graphics, game, compute in C++

### Install SDL C++:
SDL viết tắt là Simple DirectMedia Layer là một thư viện đa phương tiện, đa nền tảng bao gồm các API để thao tác với âm thanh, bàn phím, chuột, joystick, 3D hardware thông qua OpenGL, and 2D video.

SDL hổ trợ các nên tảng như Linux, Windows, Windows CE, BeOS, MacOS, Mac OS X, FreeBSD, NetBSD, OpenBSD, BSD/OS, Solaris, IRIX, and QNX.



### Install SFML C++:
### Install Boost C++:
Boost là tên một tổ chức các lập trình viên C++ và cũng là tên bộ thư viện C++ do họ phát triển. Boost có mối liên hệ mật thiết với ủy ban chuẩn hóa C++ do Boost được thành lập bởi các thành viên của ủy ban này. Và hầu hết các thư viện C++ chuẩn tương lai điều nằm trong Boost.

+ Build Boost C++:
  + Download [Boost C++](https://dl.bintray.com/boostorg/release/1.67.0/source/boost_1_67_0.zip) và extract it to folder
  + Mở **Developer Command Prompt For VS2015** của Visual Studio 2015 hoặc theo phiên bản của Visual Studio của anh (chị) 
  + **Developer Command Prompt For VS2015** trỏ tới thư mục mà bạn vừa giải nén và chạy câu lệnh **bootstrap.bat**. Sau khi câu lệnh được thực thi xong thì tiếp tục gõ lệnh **b2.exe** và chờ thư viện **Boost build xong**.
  + Cấu hình project trong Visual Studio 2015:
    + Tạo một empty project C/C++
    + Click vào mục **Debug** trên thanh menu và chọn **project_name Properties**. Xong thực hiện theo các bước:
      + Bước 1:
      
      ![](https://lh3.googleusercontent.com/RUSCDgVYtiVjrQLnqXOrD0pR-kbGzj1tsIb5Bg3x9xgS6sd71kPwpDaN7FOXHPpq14pUqX7ijzRki7ei3Hos1hxaNqpgfCKbyqT1VCl81sooRRoNK0QL7r3mneUWmfP93o5gaZR36SZ2AmngkWJy0Wk4-ax8SqbqU9e0oQq-HsfrfH9S6DbSDREdG0K_-YxK6wIwlK9D96xLEkUBsTFHBZUuvvxcTf42Woh9o8tbE8298bLtw4cINzlshqp6HjIYnfWOQvVBB89SobMJ086jq3xrmkV0MZVmEkBec8BXv38CmFoHYM-TjZi_YtmzYUaPYaHe7w4gSyWUsSEeUEBPK9rikcp7xAhEZXORiTdt9rCeoYuUwX-FDy0UE9GmxrC_fTAwyEQuhJ1xMohOG9VXgJWu-f8tV4kq_67zwZ8IRdNNxPAcb8AxMsOjrW8USLr61PMZlaSR9wz3SKkESyfSdYZWg-C8arZo1rAuYxVf2lwv13ZVTEF3rkoTdwecJzxgTEiLZA6prxzufPVuqa-2v85wbXzm_JNREiZDXFpafVbTfnLyqtTYfW_CUNA6aZQVfi4FIBG8lCuvXuxCmjHiMbFOWtjDMAF1SHGAgutD4NOaqK6GHhvyY0tkrzNFetKUoaF9wDBxJB2IXyR68XjRz8oezoD4_UOZ=w812-h551-no)
      + Bước 2: Trỏ tới **thư mục boost_1_60_0** ví dụ
      
      ![](https://lh3.googleusercontent.com/w4lqUCEPJY6najN8F-hIRvMISkcJyngOAN6YfX8DqiXi3E6wHSiepwwlblXqd5G2-_w22hvntSzwlvIfgo9KzrbwenDRLxJ7_qdr5WT1CYqCukcTTdJknCdBTFNLPRfy1NBbHjHMPYakPEya7yKKdjeTcOB67120Yt_59sVlqB-EzKsjQBJjJEQ4Yyt1a7XBmVHvOTBj3i9up8xQGPDTQ7_VEq_f0mTtEjPiQ87PkxRl17BLLvp1l3nvl0VJsWyGbWqiWrIfjMYFmjwPSt9f91vrbVuE3HE807XPp06GG_55V8usCtMdKVwq2w29F9sWyLLOP30JyQtaP7nr3BCnVYlgt-HQIsu1bgdKXOZxK7DFCchEulZRWTBFGfSJk0Yc_Lwt4QofjfC1quIsJoTD_dfiTa7WouFDtezLUEuueRYBBIC27I0o67jIoBmIIc61ZdEfXoGpxtw6Egjuw6Mq-arITlMCwRGrYIjoFkTgNsxQ5KIcGk2Kf6VH970bpCK4zF_PSprlbhsw_ca6fEsd0FUuRjoTNTj19jIg-ikdjEq-f8JohUfR8RjQF-jy4MA6FNTqMJtwqGAiX0w_vpg_ZqYnMv-hAcpGXqTQGbKBvjH5jJJYn-5nytq0RBBzWOOD80gzSGOuIYn3J-ltyJrBYq6QL-Rb4nkM=w821-h425-no)
      + Bước 3:
      
      ![](https://lh3.googleusercontent.com/agNoPp0x8clr48GvUNHe2WJ5tX5Vw0TSuRZ19nhiH24F8fsIv0hOd7chwwJRgxTmwO50s7edhrwiZ6WL0DoJ4P4FWM4f620-p6GdLV4Qx24rHFWRL66uECHpp3LFnPJp_gC2pTS3QURODzve1xsu4eJk3iZJTFSSs2iTuuqMLtdiAMSqyzdtNjAedJuqdo1q0H0MzmzXhTh2tZ4CmlbtMl2jl139CmfX5uZSnvY7lBYIR_ELRM4gBg4RKuBOU6oZV1XG93h1fxXSf574U4EFCtFf-5GvMXF-e2Pg2bcym85vscMs94sEirx3bTkuocpeiJ7UMtYCgzcdJAyOkrSu-wdrY2bEq99Ra9I_Ls7IdHKMjE9bMfLCCFpt9Mh-ey3MAan69smGxvrXPCzzcdv_vgxShkbbyeRz1rmvitpZUfQMcLsQ_ZFY_gyrZmPTRqJt3A1Oioy1Aa9OZNjG0ST1QZonONc1dwEJFrTJnPV4AjzmfpIpjfJzfnll3HuXVIxvZbA0YQmvDjCX8qRjObaLudiCDta97keY7CwQPCd__ZXq1ahGrKVc8sw7b6dvsUYEAor95jPAkdtb8cWKD_qHqQt348JTMjPoaJx32-jBWPF9wQm7XfUCQ3fAowPoV6fIWwZMrxhvLhNr617TIqexZo2Ypg98OVrT=w820-h507-no)
      
      + Bước 4: Trỏ tới **thư mục boost_1_60_0/stage/lib** ví dụ
      
      ![](https://lh3.googleusercontent.com/pe-U6hGMCdBohhLfrwksLPCo1H4994W1OoLfzOXJ8D746oO5BQnVa0ZTkLL4JsmhmJc83KB5L2l3ZuN4IKi2JbT3_JogVtdSsBJDDK8j1tw3d1f7i-7VAokAqJIIKjdYvnAQqSssZS8ofCCEN4KGMg2C3-PGGHA1tSsJ8O3-xUipXmXJtRTlRRKdqJU9guXXegtep9ES2ee-Qz5bftEYiWr8ZBgP_zlUpspFJ3waBtJxEhwAvfVArgPvVYbdFCBtnTe-H7DvRcwHnG_8uKCJk3KwNDt7lEkprpr_L0oejNPd8dRbFEWh700r1X2zJiBwtpl8ZE6LRIqJjbcxCDT-KzarrkLfU0lSrZ1f7y06sgMqetMPC50GVAIt5jJ8L8oZUtB5V9OqnOPKbYIku5XsWx4GdJcVzToRv1P-k3ZyGQnti3Z4eIZWRGByvx7aKeyvjD6lRnGN397VKRsmZ83wewX8xmzCMXwOQ5FzLA-2Yxn1bOO4oQWQjZ5F0vAzgS8I3JyU6rWBiy6W0VhXefsizLASpzQytkH0CXnrLVNsBvOqlmsDmVcG_-iF6xpddkfX2WdTIMEqPRlYPVYTKYwhNEh2XeAzDYemWXVafL6OsCt17ulYPAsoHTMt-ntMj1Gq7aWRliTZM5iKxXSlOlqY998XOq-YbBe4=w822-h414-no)
      
      + Demo:
      
      ```cpp
      #include <iostream>
      #include <boost/filesystem.hpp>
      using std::cout;
      using namespace boost::filesystem;

      int main(int argc, char* argv[])
      {
        path p ("C:\\");
        try
        {
          if (exists(p))
          {
            if (is_regular_file(p))
              cout << p << " size is " << file_size(p) << '\n';

            else if (is_directory(p))
            {
              cout << p << " is a directory containing:\n";

              for (directory_entry& x : directory_iterator(p))
                cout << "    " << x.path() << '\n'; 
            }
            else
              cout << p << " exists, but is not a regular file or directory\n";
          }
          else
            cout << p << " does not exist\n";
        }

        catch (const filesystem_error& ex)
        {
          cout << ex.what() << '\n';
        }

        return 0;
      }
      ```
      
      + Kết quả:
      
      ![](https://lh3.googleusercontent.com/yEaODgtpkVAXrXhPCWV_Rsy7KXekj9kWLlQoxeGL78COfLxDaOkx8ZAHRsVvGC_ssTxial-XdIoNDtqRhem0y6-pD3OnP9-K83vLHY1PEiIps8_7Ti1a5J8qIMMYHnuL-nGTo5YcAfjLJ8jCpyQjYQj9B3tg6-O6nlFM-ngo5U5g7BF8p05VNAnZTm83xjE-PMapmJuubVSRquu0k_LTaGisDmQUOj4l8iMTYiZ60IQ5sfIZxDk184Met37r6JEsa_O_24fQtjpV0gUU5gpwSnstlIY2HsABJFFJzL_DLwMnP5VgE4KcouAjM9oznAMruFwKrxQ0tuzwae06HojC20g8O2wD1tP-dQA295pNzvN62g32hU9lDBvNDIOS4ZEwciSvWwyakbCVo2fG_PLYoAu7-ZjV8fAz5qBSDzbH7bh97Cqxhfh6uzZIBoAADHGysteRjvcGyoKW5Tr-U3krr1hh3n4acx-ge8qXUK0FkIlRuP491qDB5mQ1qpNnmLnevsvIhQiKqLltn7vxVwV2HVL8B6QmHlL_fSslvVydiUxFCoWL82eIhvF1jmeC19mizrH7kmJY_B3UXvT-WuWYOg2ZAo9ezYLRa6FE3WoKUvT3yAQQXLjyhZ7mVJhanfxCaIDW2aEIPd6XOKhzGyJP-0BI3YrywYEF=w549-h532-no)
      
      + [FAQ's Boost](https://www.boost.org/users/faq.html): You can require new feature to Boost's organize
### Install OpenGL by Glew and Glfw3 in C++:

## Web framework in C++:

### [Cutelyst web framework in C++](https://cutelyst.org/):
### [CppCMS web framework in C++](http://cppcms.com/wikipp/en/page/main):
### [Silicon web framework in C++](http://siliconframework.org/):
### [TreeFrog web framework in C++](http://www.treefrogframework.org/):

## Mobile application development in C++:
### [Qt Mobile](https://www.qt.io/mobile-app-development/)
### [DragonFire SDK](http://www.dragonfiresdk.com/): Develop application Iphone in C++
