

```java
HttpPost httpPost = new HttpPost("http://www.itcast.cn");
```

当uri中无www时，get可正常爬取，而post不能。



![image-20220114120819234](C:\Users\ningyu\AppData\Roaming\Typora\typora-user-images\image-20220114120819234.png)

虽然名字相同，但是是不一样的类，有不同的方法。









![image-20220203114731208](C:\Users\ningyu\AppData\Roaming\Typora\typora-user-images\image-20220203114731208.png)

application运行不成功，把项目jdk换成1.8

[Spring抛java.lang.IllegalStateException Cannot load configuration class异常_Timber_kito的博客-CSDN博客](https://blog.csdn.net/timber_kito/article/details/117607980)









错误提示：Failed to start connector [Connector[HTTP/1.1-8080]]
错误原因：Tomcat端口被占用
解决方案（window下）：
1.cmd打开命令控制台

2.查看tomcat的所使用的端口 netstat -ano|findstr 8080

此处的“3920”为占用端口的进程号

3.杀死占用端口的进程 taskkill /pid 3920 /f

————————————————
版权声明：本文为CSDN博主「微笑的花」的原创文章，遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接及本声明。
原文链接：https://blog.csdn.net/yinzitun7947/article/details/85800708





###### @Scheduled() 设置initialDelay参数后，会报下面的错误

###### initialDelay =1000 当任务启动后，等多久执行方法

###### common-lang3工具包依赖版本问题

2022-02-10 13:56:22.402 ERROR 19236 --- [pool-1-thread-1] o.s.s.s.TaskUtils$LoggingErrorHandler    : Unexpected error occurred in scheduled task.

java.lang.NullPointerException: null
	at us.codecraft.webmagic.Spider.addRequest(Spider.java:468) ~[webmagic-core-0.7.3.jar:na]
	at us.codecraft.webmagic.Spider.addUrl(Spider.java:494) ~[webmagic-core-0.7.3.jar:na]
	at cn.itcast.job.task.JobProcessor.process(JobProcessor.java:37) ~[classes/:na]
	at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method) ~[na:1.8.0_322]
	at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62) ~[na:1.8.0_322]
	at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43) ~[na:1.8.0_322]
	at java.lang.reflect.Method.invoke(Method.java:498) ~[na:1.8.0_322]
	at org.springframework.scheduling.support.ScheduledMethodRunnable.run(ScheduledMethodRunnable.java:65) ~[spring-context-5.0.6.RELEASE.jar:5.0.6.RELEASE]
	at org.springframework.scheduling.support.DelegatingErrorHandlingRunnable.run(DelegatingErrorHandlingRunnable.java:54) ~[spring-context-5.0.6.RELEASE.jar:5.0.6.RELEASE]
	at java.util.concurrent.Executors$RunnableAdapter.call(Executors.java:511) [na:1.8.0_322]
	at java.util.concurrent.FutureTask.runAndReset$$$capture(FutureTask.java:308) [na:1.8.0_322]
	at java.util.concurrent.FutureTask.runAndReset(FutureTask.java) [na:1.8.0_322]
	at java.util.concurrent.ScheduledThreadPoolExecutor$ScheduledFutureTask.access$301(ScheduledThreadPoolExecutor.java:180) [na:1.8.0_322]
	at java.util.concurrent.ScheduledThreadPoolExecutor$ScheduledFutureTask.run(ScheduledThreadPoolExecutor.java:294) [na:1.8.0_322]
	at java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1149) [na:1.8.0_322]
	at java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:624) [na:1.8.0_322]
	at java.lang.Thread.run(Thread.java:750) [na:1.8.0_322]



