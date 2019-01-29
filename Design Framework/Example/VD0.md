+ C source với tên **demo.c**:

```cpp
#include<stdio.h>
void greeting_en()
{
	printf("Hello world\n");
}
void greeting_ja()
{
	printf("こ ん に ち は\n");
}
void greeting_vi()
{
	printf("Xin chào các bạn\n");
}



int main(int argc, char* argv[])
{
	greeting_en();
	return 0;
}
```

+ CMakeLists.txt:

```
cmake_minimum_required(VERSION 3.0)

set(CMAKE_BUILD_TYPE Debug)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++14")
project (demo)
add_executable(
	demo 
	demo.c
)
```
