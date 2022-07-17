### Stream流

1.获取方法

2.中间过滤，去重  （方法.方法）

3.end



1.获取方法 条件：单列集合 双列集合 数组 同种数据类型的多个数据

单列集合：把数据加入list中 调用stream方法输出即可

双列集合：构造HashMap 1.keySet/entrySet获取

数组：定义一个数组后 Arrays.stream(arr)

同种数据类型的多个数据：stream.of(放数据)

2.中间方法 filter 

a.命名内部类*Predicate接口的* test 里面加一个判断 ture则留下

b.lambda表达式 (String s)->{判断表达式}

 其他中间方法

​               a.list.stream().limit(x).forEach(s -> System.***out***.println(s));  截取从前往后x个数据输出

b.list.stream().skip(x).forEach(s -> System.***out***.println(s));跳过前x个输出后面的

c.*concat*(stream1, stream2); 把两个stream合起来

d.stream().distinct()去重

3.终结方法

a.forEach()    内只有一个accept方法 在accept中写业务

b.count()返回流中的元素数

收集方法 collect

filter(条件).collect(Collectors.*toList*())//把过滤好的数据 放到新的集合内 可以有重复

filter(条件).collect(Collectors.*toSet*())//没重复的新数据

collect(Collectors.*toMap*()) //把数据添加到Map集合