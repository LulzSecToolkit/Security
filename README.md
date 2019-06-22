# Security
一个小洞洞，不喜欢写很多废话，下面的描述也是。

# 小介绍
无意中在谷ge上搜索到了提供在线DDOS攻击的站点，感觉好好奇哦，这玩意是不是可以改变世界？

URL：http://www.ddos.rip/

这里是测评介绍，感觉挺丰富且价格也不是很贵，然后对于我们这些搬砖的攻城狮而言，花钱是不可能的，一定是不可能的！

# 过程
$SQLCheckLost = $odb -> prepare("SELECT COUNT(*) FROM `users` WHERE `username` = :username AND `email` = :mail AND `scode` = :scode ");
$SQLCheckLost -> execute(array(':username' => $username, ':mail' => $mail, ':scode' => $scode));
$countLost = $SQLCheckLost -> fetchColumn(0);
if ($countLost > 0)
{
function generarCodigo($longitud) {
 $key = '';
 $pattern = '1234567890abcdefghijklmnopqrstuvwxyz';
 $max = strlen($pattern)-1;
 for($i=0;$i < $longitud;$i++) $key .= $pattern{mt_rand(0,$max)};
 return $key;
}

几乎全部的文件都是通过预处理进行SQL传递，这玩意跟注入一直就是死对头，但是在SERVERS.PHP这玩意中没有估计到，虽然也是预处理，但是并没有通过赋值操作。
# Payload

server.php?sv=A1%%23' 将SQL语句闭合，然后你们懂的。
/ajax/servers.php?sv=A1%%27%20UNION%20ALL%20SELECT%20user()%23-- Next You K

# 影响

这样说吧，百分之七十的DDOS在线攻击网站都存在......g
谷x搜索:
https://www.google.com/search?ei=IO0NXaHYIIzdvgT2vq3ABg&q=ddos%E7%BD%91%E9%A1%B5%E7%AB%AF&oq=ddos%E7%BD%91%E9%A1%B5%E7%AB%AF&gs_l=psy-ab.12...853628.857136..858562...0.0..0.1153.1153.7-1......0....1..gws-wiz.XQGEBD9xDU0


# 结构

```
├─@
├─admin
├─ajax
│  ├─Crypt
│  ├─File
│  ├─js
│  ├─Math
│  └─Net
├─apikey
├─assets
│  ├─images
│  └─user
│      ├─css
│      ├─fonts
│      └─js
├─css
├─fonts
├─images
├─js
├─picture
└─user
```

这种垃圾的架构我也是醉了，虽然我不会ThinkPhp审计......
@ 文件夹主要是Config文件以及全局函数文件
admin 就不说了，此文件夹下也存在着相同的漏洞，但是对于黑盒而言，此漏洞是不存在的，因为TMD的后台根本就不会让你找到
ajax 主要以usercp为主，以及前台登录的login，以及servers
apikey 通过前端获取命令然后通过api向发包机发送指令
下面几个文件夹可以无视

# 么么哒

奇安信(原360企业安全)高级攻防部招聘

红队方向、渗透测试、还有一些你喜欢做的事情.....

usernameandpwd@protonmail.ch
