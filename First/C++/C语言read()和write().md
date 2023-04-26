1.都位于<unistd.h>中

read()函数

原型：ssize_t read(int fd,void*buf,size_t count)
参数说明：
fd:      是文件描述符，对应0
buf:     为读出数据的缓冲区；
count:   为每次读取的字节数（是请求读取的字节数，读上来的数据保
         存在缓冲区buf中，同时文件的当前读写位置向后移）
```c
int num;
read(0,&num,4);
```


write()函数

原型：ssize_t write(int fd,void*buf,size_t count)

参数说明：

fd:      是文件描述符，对应1
buf:     需要写入的数据，通常为字符串；
count:   每次写入的字节数

```c
char* ch = "hello world\n";
int len = strlen(ch);
write(1,ch,len);
```
