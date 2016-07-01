                                              工作总结
1调试接口的时候，url路径中的空格和双引号的不完全。空格存在与url路径的前面和后面，还有就是url中间有时候会输入非半角符号的字符
2.在代码中，存取变量时候的前后不一致，细节问题，害死人，值得深思
3.在布局文件的命名中，老是出现有空格，在名字的前面或者是中间的部位，自己老是不容易发现的
4.在logcat中，没有详细的日志打印出的时候，控制台会有相关的日志信息，工作中应该学会自己查找错误。
5.super方法老是忽略，查找问题看logcat日志不够细心，不能从中看到更加详细的信息
6singleTask的困扰：startActivityForResult（）方法的发起者activity不能是singleTask型的，这样无论怎么传递值都是传递不过去的
7一个activity的启动类型是singleTask的话，getIntent（）获取不到intent（）只能是用onNewIntent()方法可以得到
8eclicpse运行慢，困扰了好长时间，突然有时间，百度了一下，居然还是可以手动的修改eclipse的.ini文件，可以提高eclipse的运行速度
9，车大师：return关键字的使用，在登录时如果任何一个编辑框或者是之前的逻辑出现了错误，展示错误提示的时候都应该return掉，而不应该程序继续运行。按钮的可点击性逻辑跟随不是很紧
10.“”字符串的判断方式，我的那种方式会引起空指针异常

二。团车养车
1，轮播图：currentItem初始化值是0 ，但是在启动任务去改变currentItem的值的时候，需要重新为其赋值，不然，他的值一直都是初始化值，一直没有改变
2，轮播图播放的异常快：
3，虚线的画法：宽度必须未2dp .android:width="1dp"   不知道为什么虚线的高度一定需要这句话与size标签一起使用，而且是width是1，height是2.不然线展示出来不正常，同时一定需要关闭硬件加速的代码，不然，虚线还是不展示。
4，fragment嵌套fragment时，底部tab切换出现内部fragment内容不展示，
    解决：把tab对应的viewPage对应的fragment改为一个view,展示在viewPage的各个条目中。
5.优惠券列表页中的listView的复用产生的bug：抵扣券在一开始展示的时候是蓝色，在向上滑动的时候就展示成了灰色，还有就是listView的每一个item,在复用的时候，都会复用上次的数据（背景图片，以及上面的文字）
解决办法：在每一次不同的状态切换时都要手动的去设置item中的数据，
6.gradlew assembleRelease gradlew命令打包
7.netstat -ano|findstr "5037"  查看端口占用情况
8 .AsyncTask<Params,Void,Result>
    Params:异步任务加载时传递的参数
    Void：异步任务执行的时候的进度提示
    Result：异步任务执行返回的结果
三。望洲云：
1.ViewPager的问题：viewPagers实例每一个item，写测试代码不能添加同一个view，会出现图片只会展示一次，再次划回来时就不见的了bug。
