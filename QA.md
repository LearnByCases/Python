Python中的time模块和datetime模块中的time类的功能有何区别？
* time模块主要是用于处理Unix时间戳，即从1970年1月1日开始的秒数。它提供了一些操作系统层面的时间函数，如获取当前时间，格式化时间，解析时间字符串等。它的日期范围被限制在1970-2038年之间。
* 而datetime模块则提供了更多实用的函数，可以理解为datetime基于time进行了封装。

  它包含了几类： 
  * timedelta：主要用于计算时间跨度； 
  * tzinfo：时区相关； 
  * time：只关注时间；
    * datetime模块的time类是用于表示一天中的某个时刻，不包含日期信息。它提供了一些对象化的方法，如获取小时，分钟，秒等属性，比较时间大小，替换时间部分等。它可以和datetime模块的其他类如date和datetime配合使用。
  * date：只关注日期； 
  * datetime：同时有时间和日期。

  在实际使用中，用得比较多的是datetime.datetime和datetime.timedelta。



可变对象与不可变对象？
* 可变对象是指对象的内容可以改变，例如list、dict、set等。
  * 当可变对象的内容发生变化时，对象的id值不变，但是value值会变。
* 不可变对象是指对象的内容不可以改变，例如int、float、bool、str、tuple等。
  * 当不可变对象的内容发生变化时，会创建一个新的对象，对象的id值和value值都会变。

Python中的所有对象都是引用类型，即变量存储的是对象的引用（地址），而不是对象本身。所以对于可变对象和不可变对象，要注意区分引用和内容的关系。