# MySecKill
高可用&高并发&高一致

0、高可用--过滤机制
     
       登录过滤-->获取秒杀路径频率限制-->秒杀路径校验过滤-->内存标记秒杀结束过滤-->重复秒杀过滤-->预减库存-->异步下单
     
1、超卖避免--Redis减库存

2、恶意请求--请求频率限制

3、链接暴露--秒杀URL动态化，URL校验

4、按钮控制--秒杀前不可用

5、限流--后端限流，当库存减为0后直接return

6、库存预热--秒杀商品信息初始化到Redis库

7、流量削峰--MQ异步下单

8、身份拦截--登录过滤
