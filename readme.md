miniz-cpp
=========



fork from [miniz-cpp](https://github.com/tfussell/miniz-cpp)

and rename file from zip_file.hpp to miniz_cpp.hpp



update miniz to v2.2.0 from [miniz](https://github.com/richgel999/miniz)




<br/>
<br/>
Read from zip file

```cpp

#include <miniz_cpp.hpp>
int main()
{
    miniz_cpp::zip_file file("test.zip");
    file.printdir();

    return 0;
}

```

<br/>
Write to zip file 

```cpp

#include <miniz_cpp.hpp>
int main()
{
    miniz_cpp::zip_file file;
    file.writestr("file1.txt", "this is file 1");
    file.writestr("file2.txt", "this is file 2");
    file.writestr("file3.txt", "this is file 3");
    file.writestr("file4.txt", "this is file 4");
    file.writestr("file5.txt", "this is file 5");
    file.save("test.zip");
    
    return 0;
}

```

<br/>
Streams

```cpp
#include <miniz_cpp.hpp>
int main()
{
    std::ifstream stm("test.zip");
    miniz_cpp::zip_file file;
    file.load(ss);
    file.printdir();
    
    return 0;
}
```
