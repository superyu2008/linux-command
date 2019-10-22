# curl
===

利用URL规则在命令行下工作的文件传输工具

## 补充说明

**curl命令** 是一个利用URL规则在命令行下工作的文件传输工具。它支持文件的上传和下载，所以是综合传输工具，但按传统，习惯称curl为下载工具。作为一款强力工具，curl支持包括HTTP、HTTPS、ftp等众多协议，还支持POST、cookies、认证、从指定偏移处下载部分文件、用户代理字符串、限速、文件大小、进度条等特征。做网页处理流程和数据检索自动化，curl可以祝一臂之力。

## 语法

```shell
curl(选项)(参数)
```

## 选项说明

|选项  | 功能 |
| --- | --- |
| -a/--append | 上传文件时，附加到目标文件 |
| -A/--user-agent <string> | 设置用户代理发送给服务器 |
| -anyauth | 可以使用“任何”身份验证方法 |
| -b/--cookie <name=string/file> | cookie字符串或文件读取位置 |
| --basic | 使用HTTP基本验证 |
| -B/--use-ascii | 使用ASCII /文本传输 |
| -c/--cookie-jar <file> | 操作结束后把cookie写入到这个文件中 |
| -C/--continue-at <offset> | 断点续传 |
| -d/--data <data> | HTTP POST方式传送数据 |
| --data-ascii <data> | 以ascii的方式post数据 |
| --data-binary <data> | 以二进制的方式post数据 |
| --negotiate | 使用HTTP身份验证 |
| --digest | 使用数字身份验证 |
| --disable-eprt | 禁止使用EPRT或LPRT |
| --disable-epsv | 禁止使用EPSV |
| -D/--dump-header <file> | 把header信息写入到该文件中 |
| --egd-file <file> | 为随机数据(SSL)设置EGD socket路径 |
| --tcp-nodelay | 使用TCP_NODELAY选项 |
| -e/--referer | 来源网址 |
| -E/--cert <cert:[passwd]> | 客户端证书文件和密码 (SSL) |
| --cert-type <type> | 证书文件类型 (DER/PEM/ENG) (SSL) |
| --key <key> | 私钥文件名 (SSL) |
| --key-type <type> | 私钥文件类型 (DER/PEM/ENG) (SSL) |
| --pass <pass> | 私钥密码 (SSL) |
| --engine <eng> | 加密引擎使用 (SSL). "--engine list" for list |
| --cacert <file> | CA证书 (SSL) |
| --capath <directory> | CA目录 (made using c_rehash) to verify peer against (SSL) |
| --ciphers <list> | SSL密码 |
| --compressed | 要求返回是压缩的形势 (using deflate or gzip) |
| --connect-timeout <seconds> | 设置最大请求时间 |
| --create-dirs | 建立本地目录的目录层次结构 |
| --crlf | 上传是把LF转变成CRLF |
| -f/--fail | 连接失败时不显示http错误 |
| --ftp-create-dirs | 如果远程目录不存在，创建远程目录 |
| --ftp-method [multicwd/nocwd/singlecwd] | 控制CWD的使用 |
| --ftp-pasv | 使用 PASV/EPSV 代替端口 |
| --ftp-skip-pasv-ip | 使用PASV的时候,忽略该IP地址 |
| --ftp-ssl | 尝试用 SSL/TLS 来进行ftp数据传输 |
| --ftp-ssl-reqd | 要求用 SSL/TLS 来进行ftp数据传输 |
| -F/--form <name=content> | 模拟http表单提交数据 |
| --form-string <name=string> | 模拟http表单提交数据 |
| -g/--globoff | 禁用网址序列和范围使用{}和[] |
| -G/--get | 以get的方式来发送数据 |
| -H/--header <line> | 自定义头信息传递给服务器 |
| --ignore-content-length | 忽略的HTTP头信息的长度 |
| -i/--include | 输出时包括protocol头信息 |
| -I/--head | 只显示请求头信息 |
| -j/--junk-session-cookies | 读取文件进忽略session cookie |
| --interface <interface> | 使用指定网络接口/地址 |
| --krb4 <level> | 使用指定安全级别的krb4 |
| -k/--insecure | 允许不使用证书到SSL站点 |
| -K/--config | 指定的配置文件读取 |
| -l/--list-only | 列出ftp目录下的文件名称 |
| -L/--location | 跟随页面重定向  |
| --limit-rate <rate> | 设置传输速度 |
| --local-port<NUM> | 强制使用本地端口号 |
| -m/--max-time <seconds> | 设置最大传输时间 |
| --max-redirs <num> | 设置最大读取的目录数 |
| --max-filesize <bytes> | 设置最大下载的文件总量 |
| -M/--manual | 显示全手动 |
| -n/--netrc | 从netrc文件中读取用户名和密码 |
| --netrc-optional | 使用 .netrc 或者 URL来覆盖-n |
| --ntlm | 使用 HTTP NTLM 身份验证 |
| -N/--no-buffer | 禁用缓冲输出 |
| -o/--output <file>| 将文件保存为命令行中指定的文件名<file>的文件中 |
| -O/--remote-name | 使用URL中默认的文件名保存文件到本地 |
| -p/--proxytunnel | 使用HTTP代理 |
| --proxy-anyauth | 选择任一代理身份验证方法 |
| --proxy-basic | 在代理上使用基本身份验证 |
| --proxy-digest | 在代理上使用数字身份验证 |
| --proxy-ntlm | 在代理上使用ntlm身份验证 |
| -P/--ftp-port <address> | 使用端口地址，而不是使用PASV |
| -q | 作为第一个参数，关闭 .curlrc |
| -Q/--quote <cmd> | 文件传输前，发送命令到服务器 |
| -r/--range <range> | 检索来自HTTP/1.1或FTP服务器字节范围 |
| --range-file | 读取（SSL）的随机文件 |
| -R/--remote-time | 在本地生成文件时，保留远程文件时间 |
| --retry <num> | 传输出现问题时，重试的次数 |
| --retry-delay <seconds> | 传输出现问题时，设置重试间隔时间 |
| --retry-max-time <seconds> | 传输出现问题时，设置最大重试时间 |
| -s/--silent | 静默模式。不输出任何东西 |
| -S/--show-error | 显示错误 |
| --socks4 <host[:port]> | 用socks4代理给定主机和端口 |
| --socks5 <host[:port]> | 用socks5代理给定主机和端口 |
| --stderr <file> |   |
| -t/--telnet-option <OPT=val> | Telnet选项设置 |
| --trace <file> | 对指定文件进行debug |
| --trace-ascii <file> | Like --跟踪但没有hex输出 |
| --trace-time | 跟踪/详细输出时，添加时间戳 |
| -T/--upload-file <file> | 上传文件 |
| --url <URL> | Spet URL to work with |
| -u/--user <user[:password]> | 设置服务器的用户和密码 |
| -U/--proxy-user <user[:password]> | 设置代理用户名和密码 |
| -w/--write-out [format] | 什么输出完成后 |
| -x/--proxy <host[:port]> | 在给定的端口上使用HTTP代理 |
| -X/--request <command> | 指定什么命令 |
| -y/--speed-time | 放弃限速所要的时间，默认为30 |
| -Y/--speed-limit | 停止传输速度的限制，速度时间 |
| -z/--time-cond | 只下载指定时间以后更新的文件  |

## 实例

### **文件下载**

curl命令可以用来执行下载、发送各种HTTP请求，指定HTTP头部等操作。如果系统没有curl可以使用`yum install curl`安装，也可以下载安装。curl是将下载文件输出到stdout，将进度信息输出到stderr，不显示进度信息使用`--silent`选项。

```shell
curl URL --silent
```

这条命令是将下载文件输出到终端，所有下载的数据都被写入到stdout。

使用选项`-O`将下载的数据写入到文件，必须使用文件的绝对地址：

```shell
# 将文件保存到本地并命名为gettext.html
curl -O http://www.gnu.org/software/gettext/manual/gettext.html
```

选项`-o`将下载数据写入到指定名称的文件中，并使用`--progress`显示进度条：

```shell
# 将文件下载到本地并命名为mygettext.html
curl -o mygettext.html http://www.gnu.org/software/gettext/manual/gettext.html -progress
######################################### 100.0%
同样可以使用重定向">"对输出进行转向输出
curl  http://www.gnu.org/software/gettext/manual/gettext.html -progress > mygettext.html
```
**同时下载多个文件**
```
curl -O URL1 -O URL2
```

**限制下载速度和下载配额**
通过 **--limit-rate** 选项对CURL的最大下载速度进行限制
单位bytes/second，用k/K（千字节），m/M（兆字节）和g/G指定下载速度限制。

```
# 下载速度最大不会超过1000B/second
curl --limit-rate 1000B -O http://www.gnu.org/software/gettext/manual/gettext.html
```

使用`--max-filesize`指定可下载的最大文件大小：

```shell
curl URL --max-filesize bytes
```
如果文件大小超出限制，命令则返回一个非0退出码，如果命令正常则返回0。


**只下载指定日期后更新的文件**
使用 **-z** 选项下载文件在指定日期内修改过，就进行下载，否则不下载。
```
# 若yy.html文件在2011/12/21之后有过更新才会进行下载
curl -z 21-Dec-11 http://www.example.com/yy.html
```

**重定向页面的访问**
默认情况下CURL不会发送HTTP Location headers(重定向)。使用 `-L` 选项当一个被请求页面移动到另一个站点时，会发送一个HTTP Loaction header作为请求，然后将请求重定向到新的地址上。
例如：访问http://centos.org 会重定向到 https://centos.org
```
# curl http://centos.org 
<html>
<head><title>301 Moved Permanently</title></head>
<body bgcolor="white">
<center><h1>301 Moved Permanently</h1></center>
<hr><center>nginx/1.12.2</center>
</body>
</html>

# 使用-L选项访问
# curl http://centos.org -L
<!DOCTYPE html>
<html>
  <head>
  <meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
   此处省略
   ```

   **断点续传**

   curl能够从特定的文件偏移处继续下载，它可以通过指定一个偏移量来下载部分文件：

   ```shell
   curl URL/File -C 偏移量

   #偏移量是以字节为单位的整数，如果让curl自动推断出正确的续传位置使用-C -：

   # 当文件在下载完成之前结束该进程
   $ curl -O http://www.gnu.org/software/gettext/manual/gettext.html3 
   ############## 20.1%

   # 通过添加-C选项继续对该文件进行下载，已经下载过的文件不会被重新下载
   curl -C - -O http://www.gnu.org/software/gettext/manual/gettext.html7 
   ############### 21.1%
   ```

   **使用curl设置来源网址，参照页字符串**

   参照页是位于HTTP头部中的一个字符串，用来表示用户是从哪个页面到达当前页面的，如果用户点击网页A中的某个连接，那么用户就会跳转到B网页，网页B头部的参照页字符串就包含网页A的URL。

   使用`--referer`或 `-e` 选项指定参照页字符串：

   ```shell
   curl --referer http://www.google.com http://wangchujiang.com
   curl -e http://www.google.com http://wangchujiang.com
   ```

   **用curl设置用户代理字符串**

   有些网站访问会提示只能使用IE浏览器来访问，这是因为这些网站设置了检查用户代理，可以使用curl把用户代理设置为IE，这样就可以访问了。使用`--user-agent`或者`-A`选项：

   Chrome/77.0.3865.90

   ```shell
   curl URL --user-agent "Mozilla/5.0"
   curl URL -A "Mozilla/5.0"
   ```


   **只打印响应头部信息**

   通过大写i `-I`或者`--head`可以只打印出HTTP头部信息：

   ```shell
   [root@localhost text]# curl -I http://wangchujiang.com
   HTTP/1.1 200 OK
   Server: nginx/1.2.5
   date: Mon, 10 Dec 2012 09:24:34 GMT
   Content-Type: text/html; charset=UTF-8
   Connection: keep-alive
   Vary: Accept-Encoding
   X-Pingback: http://wangchujiang.com/xmlrpc.php
   ```

   **用curl进行认证**

   使用curl选项 -u 可以完成HTTP或者FTP的认证，可以指定密码，也可以不指定密码在后续操作中输入密码：

   ```shell
   curl -u user:pwd http://wangchujiang.com
   curl -u user http://wangchujiang.com
   ```

   **用curl设置cookies**

   使用`--cookie "COKKIES"`选项来指定cookie，多个cookie使用分号分隔：

   ```shell
   curl http://wangchujiang.com --cookie "user=root;pass=123456"
   ```
   保存与使用网站cookie信息
   ```
   # 将网站的cookies信息保存到sugarcookies文件中
   curl -D sugarcookies http://localhost/sugarcrm/index.php3
   # 使用上次保存的cookie信息
   curl -b sugarcookies http://localhost/sugarcrm/index.php
   ```
   将cookie另存为一个文件，使用`--cookie-jar`选项：

   ```shell
   curl URL --cookie-jar cookie_file
   ```

   其他HTTP头部信息也可以使用curl来发送，使用`-H`"头部信息" 传递多个头部信息，例如：

   ```shell
   curl -H "Host:wangchujiang.com" -H "accept-language:zh-cn" URL
   ```

   “域名绑定”，就是把host映射到对应的目录。如果手头有cURL，可以使用 -H 参数，在请求头信息中多写一个 Host 字段。 
   ```
   curl -H "Host: g2r.wanhui.cn" http://10.77.135.65:8080
   ```

   **使用 -X 选项指定请求的协议**
   ```
   curl -I -X DELETE https://api.github.cim
   curl -I -X GET https://api.github.cim
   curl -I -X POST https://api.github.cim
   ```

   **get请求**

   ```shell
   curl "http://www.wangchujiang.com"    # 如果这里的URL指向的是一个文件或者一幅图都可以直接下载到本地
   curl -i "http://www.wangchujiang.com" # 显示全部信息
   curl -l "http://www.wangchujiang.com" # 只显示头部信息
   curl -v "http://www.wangchujiang.com" # 显示get请求全过程解析
   ```

   **post请求**

   ```shell
   curl -d "param1=value1&param2=value2" "http://www.wangchujiang.com"
   ```
   默认情况下，通过POST方式传递过去的数据中若有特殊字符，首先需要将特殊字符转义在传递给服务器端，如value值中包含有空格，则需要先将空格转换成%20，如：
   ```
   curl -d "value%201" http://hostname.com`
   # GET
   curl -u username https://api.github.com/user?access_token=XXXXXXXXXX3
   # POST
   curl -u username --data "param1=value1&param2=value" https://api.github.com6
   # 也可以指定一个文件，将该文件中的内容当作数据传递给服务器端
   curl --data @filename https://github.api.com/authorizations
   # 指定XML文件作为数据
   curl -X POST -H 'content-type: application/xml'  -d @/apps/myxmlfile.txt http://github.api.com/authorizations
   ```
   在新版本的CURL中，提供了新的选项 --data-urlencode，通过该选项提供的参数会自动转义特殊字符。
   ```
   curl --data-urlencode "value 1" http://hostname.com
   ```




   **json格式的post请求**

   ```shell
   curl -l -H "Content-type: application/json" -X POST -d '{"phone":"13521389587","password":"test"}' http://wangchujiang.com/apis/users.json
   ```

   **通过 -T 选项可将指定的本地文件上传到FTP服务器上**
   ```
   # 将myfile.txt文件上传到服务器
   curl -u ftpuser:ftppass -T myfile.txt ftp://ftp.testserver.com
   # 同时上传多个文件
   curl -u ftpuser:ftppass -T "{file1,file2}" ftp://ftp.testserver.com
   # 从标准输入获取内容保存到服务器指定的文件中
   curl -u ftpuser:ftppass -T - ftp://ftp.testserver.com/myfile_1.txt
   ```

   **使用 -x 选项通过代理访问网站**
   ```
   curl -x proxysever.test.com:3128 http://google.co.in
   ```

   **使用 -k 选项忽略自签名的证书错误**

   **获取本机外网ip**

   ```shell
   curl ipecho.net/plain
   ```

   参考：
   http://curl.haxx.se/docs/httpscripting.html
   https://www.cnblogs.com/gbyukg/p/3326825.html
   <!-- Linux命令行搜索引擎：https://jaywcjlove.github.io/linux-command/ -->

