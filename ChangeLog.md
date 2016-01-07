## Version 0.3.1  2012-Mar-02 ##
  * 增加时间纠偏：客户端时间和服务器时间不一致时，自动根据服务器的响应进行偏移校正
  * 优化异常机制：默认方法只返回NSPException
  * SDK自定义Bean支持Integer
  * SDK自定义Map默认改为LinkedHashMap，以保证服务器返回结果的顺序性

## Version 0.3  2012-Mar-01 ##
  * 部分bug修复

## Version 0.2  2011-Dec-27 ##
  * 支持gzip压缩，节省客户端响应流量

