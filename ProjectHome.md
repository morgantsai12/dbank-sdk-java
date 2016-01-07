# 华为网盘SDK Java版 #
[华为网盘](http://www.dbank.com)为用户提供国内领先的网络存储服务，您可以通过华为网盘随时随地存取照片、视频、音乐、文档和其它任意类型的文件。文件外链、微博外链等功能可以让您轻松地将文件分享给他人。

DBank SDK 是[华为网盘开放平台](http://open.dbank.com)的Java版本封装，初衷是为了简化Android手机端应用的开发。 使用SDK，可以轻松实现数据的上传、下载、管理。

# 使用示例 #
  * 初始化VFS对象
```
String session = "xxx";
String secret = "xxx";
NSPClient nsp = new NSPClient(session, secret);
VFS vfs = nsp.service(VFS.class);
```

  * 获取子文件和目录 [nsp.VFS.lsdir](http://open.dbank.com/wiki/index.php?title=nsp.VFS.lsdir)
```
Map<String, Object> options = new HashMap<String, Object>();
// 1-files only; 2-directories only; 3-files and directories
options.put("type", 3);
String[] fields = new String[] { "name", "type", "url", "size", "md5" };
LsResult obj = vfs.lsdir("/Netdisk", fields, options);
File[] children = obj.getChildList();
```

  * 删除文件或目录[nsp.VFS.rmfile](http://open.dbank.com/wiki/index.php?title=nsp.VFS.rmfile)
```
String[] fs = new String[] { "/Netdisk/test.zip" };
Result r = vfs.rmfile(fs, false, null);
VFS.Error[] errors = r.getFailList();
```

# 帮助改进 #
  * [提新需求或者反馈BUG](http://code.google.com/p/dbank-sdk-java/issues/entry)