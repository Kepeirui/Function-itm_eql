## itm_eql 函数

### 头文件

`itm_eql.h`

### 函数原型

```c
int itm_eql(const char* selec_itm, int obj_max_itm_len, const char* obj_file_name);
```

### 参数

- `selec_itm`: 给定的用以查找的项目；
- `obj_max_itm_len`: 在文件`obj_file_name`中最长的项目的长度（单位：字节）；
- `obj_file_name`: 供查找的目标文本文件的文件名。

### 注意事项

- 目标文本文件的一行被视为一个项目，即以`'\n'`分隔项目，若您的目标文本文件非此格式，烦请稍作格式化；
- `obj_file_name`的打开格式为`"r"`，请确保目录中有此文件，否则将出错。

### 返回值

- 0: 无重复项；
- 1: 有重复项；
- -1: 在打开`obj_file_name`时出现错误。
