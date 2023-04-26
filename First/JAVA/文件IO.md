```java
void testReadFile2() throws IOException {
   String fileName = "D:\\data\\test\\newFile.txt";

   // 读取文件内容到Stream流中，按行读取
   Stream<String> lines = Files.lines(Paths.get(fileName));

   // 随机行顺序进行数据处理
   lines.forEach(ele -> {
      System.out.println(ele);
   });
}
```