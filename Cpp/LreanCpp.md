# 配置开发环境

[Visual Studio IDE - 用于编码调试和测试的 AI](https://visualstudio.microsoft.com/zh-hans/vs/)

[小熊猫C++](http://royqh.net/redpandacpp/)

[sourceforge.net/projects/orwelldevcpp/](https://sourceforge.net/projects/orwelldevcpp/)

[Visual Studio Code - The open source AI code editor](https://code.visualstudio.com/)

[MSYS2](https://www.msys2.org/)

> [!CAUTION]
>
> 注意任何程序员都会接触Linux操作系统，该系统需要自己配置所以的环境变量。因此本教程将会使用VS Code（代码） + mingw-w64 （编译）



# 你好，世界

这是一个简单的C++程序，让你了解程序如何运行。

```cpp
#include <iostream>

int main() {
	std::cout << "Hello,World!\n";
}
```



<font color="blue" size="5">头文件</font>

```cpp
#include <iostream>
```

- `#include` 是预处理指令，告诉编译器包含指定的头文件
- `<iostream>` 是C++标准输入输出流库，提供基本的输入输出功能
- **重要**：如果没有包含这个头文件，就无法使用 `std::cout` 进行输出



<font color="blue" size="5">主函数</font>

```cpp
int main()
```

- 每个C++程序必须有且只有一个 `main` 函数
- 程序执行时，操作系统会自动调用 `main` 函数作为程序的入口点

- `int` 表示函数返回一个整数值，通常用于表示程序的退出状态（0表示成功）



<font color="blue" size="5">输出语句</font>

```cpp
std::cout << "Hello, World!\n";
```

- `std::cout` 是标准输出流对象，用于向控制台输出数据
- `std` 是C++标准库的命名空间，防止命名冲突
- `<<` 是流插入运算符，将右侧的内容发送到左侧的输出流
- `\n` 是换行符，表示输出完成后换到下一行



<font color="blue" size="5">编译与运行</font>

使用MinGW-w64编译器编译程序：

```cmd
# 编译命令格式：编译器  源文件  -o  输出文件名
g++ text.cpp -o text.exe
```

- `g++`：C++编译器（专为C++设计，会自动链接C++标准库）
- `text.cpp`：源代码文件
- `-o`：指定输出文件名
- `text.exe`：生成的可执行文件



| 参数 | 解释           | 参数    | 解释     |
| ---- | -------------- | ------- | -------- |
| -o   | 指定输出文件名 | -Wall   | 打开警告 |
| -O3  | 打开优化       | -Static | 静态编译 |
|      |                |         |          |



<font color="blue" size="5">扩展</font>

```cmd
#内容输出到a.txt 但错误流等不会被放入
1.exe > a.txt
```

```cmd
#内容输出到a.txt 错误输出到b.txt
1.exe > a.txt 1>b.txt
```

```cmd
#把a.txt内容输入到1.exe
1.exe < a.txt
```

```cmd
#把a.txt内容输入到1.exe再输出到output.txt
1.exe < a.txt > output.txt
```

```cmd
#筛选，只输出hello
1.exe | find “hello”
```





> [!WARNING]
>
> 源代码 (.cpp) → 编译器处理 → 可执行文件 (.exe)





