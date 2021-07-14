在`csrc`文件夹下加入`CMakeLists.txt`，其添加了一个`u8g2`库目标，使用示例：

```cmake

add_subdirectory("u8g2/csrc")

add_executable(app.elf main.c)
target_link_libraries(app.elf
    PRIVATE
    u8g2::ls013b7dh03
    u8g2::fonts)
```

其他库说明请参照[官方](https://github.com/olikraus/u8g2)仓库。
