最好用的 Xray 一键安装脚本
2023-05-13 12:20
最好用的 Xray 一键安装脚本 & 管理脚本

介绍
最好用的 Xray 脚本

Github 地址：https://github.com/233boy/Xray

特点
快速安装
无敌好用
零学习成本
自动化 TLS
简化所有流程
屏蔽 BT
屏蔽中国 IP
使用 API 操作
兼容 Xray 命令
强大的快捷参数
支持所有常用协议
一键添加 Shadowsocks 2022
一键添加 VMess-(TCP/mKCP/QUIC)
一键添加 VMess-(WS/H2/gRPC)-TLS
一键添加 VLESS-(WS/H2/gRPC)-TLS
一键添加 Trojan-(WS/H2/gRPC)-TLS
一键添加 VLESS-XTLS-uTLS-REALITY
一键添加 VMess-(TCP/mKCP/QUIC) 动态端口
一键启用 BBR
一键更改伪装网站
一键更改 (端口/UUID/密码/域名/路径/加密方式/SNI/动态端口/等…)
还有更多…

设计理念
设计理念为：高效率，超快速，极易用

脚本基于作者的自身使用需求，以 多配置同时运行 为核心设计

并且专门优化了，添加、更改、查看、删除、这四项常用功能

你只需要一条命令即可完成 添加、更改、查看、删除、等操作

例如，添加一个配置仅需不到 1 秒！瞬间完成添加！其他操作亦是如此！

脚本的参数非常高效率并且超级易用，请掌握参数的使用

请认真往下阅读脚本的参数使用，你就会发现可以如此美妙

支持协议列表
VMess-TCP
VMess-mKCP
VMess-QUIC
VMess-H2-TLS
VMess-WS-TLS
VMess-gRPC-TLS
VLESS-H2-TLS
VLESS-WS-TLS
VLESS-gRPC-TLS
VLESS-XTLS-uTLS-REALITY
Trojan-H2-TLS
Trojan-WS-TLS
Trojan-gRPC-TLS
Shadowsocks
VMess-TCP-dynamic-port
VMess-mKCP-dynamic-port
VMess-QUIC-dynamic-port

机场推荐
如果你只是单纯的翻，墙需求，可以购买机场的，不用自己搭建什么的，省心省力。

机场推荐： Just My Socks

Just My Socks 是搬瓦工提供的 Shadowsocks & V2Ray 服务，不怕跑路，非国人商家，无须担心 IP 被墙问题。

购买教程： Just My Socks 详细图文购买教程

搭建教程
如果是新手，请看：Xray 一键搭建详细图文教程

安装
系统支持：Ubuntu，Debian，CentOS，推荐使用 Ubuntu 22，谨慎使用 CentOS，脚本可能无法正常运行！

执行如下命令：

bash <(wget -qO- -o- https://github.com/233boy/Xray/raw/main/install.sh)
安装完成
当你执行了上面的安装命令，并且没有错误提示的话，那么你就能看到类似下面的图片

Xray 脚本安装完成
脚本特意弄了一个时间显示，给反馈用来检测安装时间的…

理论上，绝大多数情况下 15 秒内会安装完成，条件允许的情况下仅需一秒即可完成安装！

超过 15 秒的你应该考虑换 VPS 了，推荐使用 搬瓦工 VPS

为方便你快速使用，脚本在安装完成后会自动创建一个 VMess-TCP 配置。

此时你可以复制 URL 到相关软件 (例如 v2rayN) 去测试一下是否正常使用。

如果无法正常使用，请尝试使用 xray add ss auto auto aes-256-gcm 添加一个 SS 来再测试一下

管理面板
安装完成后，输入 xray 就能看到管理面板，如下图片所示

Xray 脚本管理面板
提示，如果你不想执行任何功能，直接按 Enter 回车退出即可。

无法使用
无法使用一般都是两种情况，一是无法连接上端口，二是客户端内核支持有问题。

如果你的 VPS 有外部防火墙，请确保你已经开放了端口

测试端口是否能连接上：

打开：https://ping.sx/check-port

Target 写你的 VPS IP，Port 写 V2Ray 的端口，然后点击 Check，如果 REACHABILITY 显示 Timeout，那是无法连接上端口

提醒，你可以使用 xray ip 查看 VPS IP。

关闭防火墙，执行如下命令：

systemctl stop firewalld; systemctl disable firewalld; ufw disable

关闭防火墙之后再测试一下端口是否通，如果不通，你可能还有外部防火墙没关，必须要能连接上端口才能正常使用。

如果 REACHABILITY 显示 Reachable 那就是能连接上端口，那就继续

使用 xray add ss auto auto aes-256-gcm 添加一个 SS 看看能不能正常使用，如果正常使用，证明运行没有问题。

提醒，默认安装的 Xray 内核为最新版本

如果无法使用，可能是你客户端的内核太旧

请尝试使用不同的客户端进行测试；比如 v2rayN；v2rayNG 等

请尝试设置 VMessAEAD，某些客户端会有相关选项

某些客户端得把 额外id(alterid) 填写为 0；比如垃圾苹果那边的东西

请更新你的客户端 Xray 内核跟服务器端版本保持一致！

快速入门
Xray 脚本简化了很多流程，例如我们常用的是 (添加、更改、查看、删除) 配置，以下内容让你可以快速掌握使用

添加配置：

xray add -> 添加配置

xray add reality -> 添加一个 VLESS-XTLS-uTLS-REALITY 配置

xray add reality 443 auto dl.google.com -> 同上，自定义参数：端口使用 443， SNI 使用 dl.google.com

xray add ss -> 添加一个 Shadowsocks 2022 配置

xray add tcp -> 添加一个 VMess-TCP 配置

xray add kcpd -> 添加一个 VMess-mKCP-dynamic-port 动态端口配置

备注，使用 xray add 添加配置的时候，仅 *TLS 相关协议配置必须提供域名，其他均可自动化处理。

如需查看更多 add 参数用法，请查看下面的 add 说明

–

更改配置：

xray change -> 更改配置

xray change reality -> 更改 REALITY 相关配置

xray change reality sni 1.1.1.1 -> 更改 REALITY 相关配置的 SNI 为 1.1.1.1, 也可以使用 xray sni reality 1.1.1.1

xray change tcp -> 更改 TCP 相关配置

xray change tcp port auto -> 更改 TCP 相关配置的端口，端口使用自动创建，也可以使用 xray port tcp auto

xray change kcp id auto -> 更改 mKCP 相关配置的 UUID，UUID 使用自动创建，也可以使用 xray id tcp auto

如需查看更多 change 参数用法，请查看下面的 change 说明

–

查看配置：

xray info -> 查看配置

xray info REALITY -> 查看 REALITY 相关配置

xray info tcp -> 查看 TCP 相关配置

–

删除配置：

xray del -> 删除配置

xray del REALITY -> 删除 REALITY 相关配置

xray del tcp -> 删除 TCP 相关配置

提醒，谨慎使用 del 参数

–

非常棒！你已经掌握最常用的功能 (添加、更改、查看、删除)

add / change / info / del ： 添加、更改、查看、删除

对于绝大多数用户来说

使用 xray add 添加配置，使用 xray change xray info xray del 来 (更改、查看、删除) 配置即可。

提醒，如果只匹配到一个配置时则自动选择该配置，否则将显示匹配到的配置列表，要求选择其中一个配置

add
add 是一个用来添加配置的参数

备注：可选参数中使用 auto 代替即是让脚本自动化处理相关参数

用法：xray add [protocol] [args... | auto]

举例：

xray add
xray add h2
xray add ws
xray add ss
xray add tcp
xray add kcpd
xray add reality

提醒，当 可选参数 不存在时，即默认为 auto，仅 *TLS 协议配置的域名无法自动处理。

例如，xray add tcp 等于 xray add tcp auto auto auto

–

可选参数详细说明如下：

添加一个 VLESS-XTLS-uTLS-REALITY 配置
可选参数：端口，UUID，SNI
用法: xray add reality [port] [uuid] [sni]
举例:

xray add reality

xray add reality 443 auto dl.google.com -> 端口使用 443，SNI 使用 dl.google.com

–

添加一个 Shadowsocks 配置
可选参数：端口，密码，加密方式
用法：xray add ss [port] [password] [method]
举例：

xray add ss

xray add ss auto auto 2022-blake3-aes-128-gcm -> 加密方式使用 2022-blake3-aes-128-gcm

xray add ss 233 233boy aes-128-gcm -> 端口使用 233，密码使用 233boy.com，加密方式使用 aes-128-gcm

–

添加一个 Socks 配置
可选参数：端口，密码，加密方式
用法：xray add socks [port] [username] [password]
举例：

xray add socks

xray add socks 233 233boy 233boy.com -> 端口使用 233，用户名使用 233boy，密码使用 233boy.com

–

添加一个 VMess-(TCP/mKCP/QUIC) 配置
可选参数：端口，UUID，伪装类型
用法：xray add [tcp | kcp | quic] [port] [uuid] [type]
举例：

xray add tcp -> 添加一个 VMess-TCP 配置

xray add kcp -> 添加一个 VMess-mKCP 配置

xray add quic -> 添加一个 VMess-QUIC 配置

xray add tcp 233 auto http -> 端口使用 233，伪装类型使用 http

xray add kcp 234 auto dtls -> 端口使用 234，伪装类型使用 dtls

xray add quic 235 auto wechat-video -> 端口使用 235，伪装类型使用 wechat-video

–

添加一个 VMess-(TCP/mKCP/QUIC) 动态端口配置
可选参数：端口，UUID，伪装类型，动态开始端口，动态结束端口
用法：xray add [tcpd | kcpd | quicd] [port] [uuid] [type] [start] [end]
举例：

xray add tcpd -> 添加一个 VMess-TCP 动态端口配置

xray add kcpd -> 添加一个 VMess-mKCP 动态端口配置

xray add quicd -> 添加一个 VMess-QUIC 动态端口配置

xray add tcpd 223 auto http 2333 3333 -> 端口使用 233，伪装类型使用 http，动态端口使用 2333-3333

xray add kcpd auto auto dtls 2333 2444 -> 伪装类型使用 dtls，动态端口 2333-2444

xray add quicd 456 auto dtls 4567 5678 -> 端口使用 456，伪装类型使用 dtls，动态端口使用 4567-5678

–

添加一个 VMess-(WS/H2/gRPC)-TLS 配置
可选参数：域名，UUID，路径
用法: xray add [ws | h2 | grpc] [host] [uuid] [path]
举例:

xray add ws -> 添加一个 VMess-WS-TLS 配置

xray add h2 -> 添加一个 VMess-H2-TLS 配置

xray add grpc -> 添加一个 VMess-gRPC-TLS 配置

xray add ws 233boy.com -> 域名使用 233boy.com

xray add h2 233boy.com auto /h2 -> 域名使用 233boy.com，路径使用 /h2

xray add grpc 233boy.com auto /grpc -> 域名使用 233boy.com，路径使用 /grpc

–

添加一个 VLESS-(WS/H2/gRPC)-TLS 配置
可选参数：域名，UUID，路径
用法: xray add [vws | vh2 | vgrpc] [host] [uuid] [path]
举例:

xray add vws -> 添加一个 VLESS-WS-TLS 配置

xray add vh2 -> 添加一个 VLESS-H2-TLS 配置

xray add vgrpc -> 添加一个 VLESS-gRPC-TLS 配置

xray add vws 233boy.com -> 域名使用 233boy.com

xray add vh2 233boy.com auto /h2 -> 域名使用 233boy.com，路径使用 /h2

xray add vgrpc 233boy.com auto /grpc -> 域名使用 233boy.com，路径使用 /grpc

–

添加一个 Trojan-(WS/H2/gRPC)-TLS 配置
可选参数：域名，UUID，路径
用法: xray add [tws | th2 | tgrpc] [host] [uuid] [path]
举例:

xray add tws -> 添加一个 Trojan-WS-TLS 配置

xray add th2 -> 添加一个 Trojan-H2-TLS 配置

xray add tgrpc -> 添加一个 Trojan-gRPC-TLS 配置

xray add tws 233boy.com -> 域名使用 233boy.com

xray add th2 233boy.com auto /h2 -> 域名使用 233boy.com，路径使用 /h2

xray add tgrpc 233boy.com auto /grpc -> 域名使用 233boy.com，路径使用 /grpc

–

提醒，xray add [protocol] 的 protocol 也可以换完整的协议名称，名称看上面的支持协议列表

举例，xray add Shadowsocks 跟 xray add ss 是一样的，但当然还是用简化的名称吧，简单好记。

再说一遍，当可选参数不存在时默认是自动化处理的 (除了 *TLS 的配置必须提供域名)，如非必要，可以省去使用可选参数的。

所以，绝大多数情况下，只要加上协议即可，举例： xray add tcp，xray add kcp，xray add kcpd

no-auto-tls
no-auto-tls 参数跟 add 参数用法一样，但禁止自动配置 TLS, 可用于 *TLS 相关协议

用法：xray no-auto-tls [protocol] [args... | auto]

举例：

xray no-auto-tls
xray no-auto-tls ws
xray no-auto-tls vh2 233boy.com
xray no-auto-tls tgrpc 233boy.com

提醒，如果你想要手动配置 TLS，请使用此选项，例如你想要用 NGINX 实现 TLS

帮助说明：Xray 脚本 no-auto-tls 参数帮助说明

[name]
试想一虾，如果你当前有 233 个 VMess-TCP 配置的时候，如何快速选择其中一个配置呢

当你有多个配置时，你可以使用 [name] 关键词用来匹配相关配置，以便于快速执行 更改，查看，删除 等操作

推荐使用 端口 或者 域名 来匹配，这样更加容易筛选相关配置。

请往下查看会使用到 [name] 的举例

提醒，如果只匹配到一个配置时则自动选择该配置，否则将显示匹配到的配置列表，要求选择其中一个配置

change
change 是一个用来更改配置的参数

用法: xray change [name] [option] [args... | auto]

提醒：不同的配置可提供更改的相关选项是不同的

[option] 名称及选项说明参数如下：

名称	可选参数	用途	auto
dp, dynamicport	[start] [end]	更改动态端口	是
full	[…]	更改多个参数	其他
id	[uuid]	更改 UUID	是
host	[domain]	更改域名	-
port	[port]	更改端口	是
path	[path]	更改路径	是
passwd	[passowrd]	更改密码	是
key	[Private key] [Public key]	更改密钥	是
type	[type]	更改伪装类型	是
method	[method]	更改加密方式	是
sni	[domain]	更改 serverName	是
seed	[seed]	更改 mKCP seed	是
new	[…]	更改协议	其他
web	[domain]	更改伪装网站	-
备注，支持 auto 的即是可以将可选参数设置为 auto，以执行自动更改相关参数

如果 auto 为其他，可选参数请参考 add 参数用法，full 类似于 xray add 当前协议 [...]，new 类似于 xray add [...]

举例:

xray change -> 更改配置

xray change tcp -> 更改一个 tcp 相关的配置

xray change tcp port 233 -> 更改一个 TCP 配置的端口为 233

xray change tcp port auto -> 更改一个 TCP 配置的端口，并且端口自动创建

xray change kcp id auto -> 更改一个 mKCP 配置的 UUID，并且 UUID 自动创建

xray change kcp dp auto -> 更改一个 mKCP 配置的动态端口，并且动态端口自动创建

xray change kcp dp 233 332 -> 更改一个 mKCP 配置的动态端口为 233-332

xray change tls host 233boy.com -> 更改一个 tls 配置的域名为 233boy.com

xray change tls web example.com -> 更改一个 tls 配置的伪装网站为 example.com

xray change reality sni 1.1.1.1 -> 更改一个 reality 配置的 SNI 为 1.1.1.1

提醒， [option] 名称也支持直接使用

用法：xray [option] [name] [...]

举例：

xray id -> 更改 UUID

xray port -> 更改 端口

xray port tcp 233 -> 更改一个 tcp 配置的端口为 233

xray id tcp -> 更改一个 tcp 配置的 UUID

xray id tcp auto -> 更改一个 tcp 配置的 UUID，并且 UUID 自动创建

xray dp kcp auto -> 更改一个 mKCP 配置的动态端口，并且动态端口自动创建

xray dp kcp 233 332 -> 更改一个 mKCP 配置的动态端口为 233-332

xray host tls 233boy.com -> 更改一个 tls 配置的域名为 233boy.com

xray web tls example.com -> 更改一个 tls 配置的伪装网站为 example.com

xray sni reality 1.1.1.1 -> 更改一个 reality 配置的 SNI 为 1.1.1.1

更改配置的选项较多，就不一个一个举例了，绝大多数情况下使用 xray change 即可

info
info 是一个用来查看配置的参数

用法: xray info [name]

举例:

xray info -> 查看配置

xray info tcp -> 查看一个 tcp 配置

xray info kcp -> 查看一个 kcp 配置

xray info tls -> 查看一个 tls 配置

url
url 是一个生成配置的 URL 链接的参数

用法: xray url [name]

举例:

xray url -> 查看配置的 URL 链接

xray url tcp -> 查看一个 tcp 配置的 URL 链接

xray url kcp -> 查看一个 kcp 配置的 URL 链接

xray url tls -> 查看一个 tls 配置的 URL 链接

qr
qr 是一个用来生成配置的二维码的参数

用法: xray qr [name]

举例:

xray qr -> 查看配置的二维码

xray qr tcp -> 查看一个 tcp 配置的二维码

xray qr kcp -> 查看一个 kcp 配置的二维码

xray qr tls -> 查看一个 tls 配置的二维码

del
del 是一个用来删除配置的参数

用法: xray del [name]

举例:

xray del -> 删除配置

xray del tcp -> 删除一个 tcp 配置

xray del kcp -> 删除一个 kcp 配置

xray del tls -> 删除一个 tls 配置

谨慎使用此选项

ddel
ddel 是一个用来删除多个配置的参数

用法: xray ddel [name...]

举例:

xray ddel -> 删除配置

xray ddel tcp kcp -> 同时删除一个 tcp，一个 kcp 配置

提醒，此处的 [name] 只有匹配到相关配置是唯一时，才会执行删除

例如，假设你当前有两个 tcp 配置，使用 xray ddel tcp 是不会删除任何文件的

谨慎使用此选项

gen
gen 参数跟 add 参数用法一样，但是 gen 参数只返回 JSON 内容，不会创建配置，仅供测试使用

用法：xray gen [protocol] [args... | auto]

举例：

xray gen ss
xray gen tcp
xray gen kcpd
xray gen reality 2333
xray gen ws 233boy.com

genc
genc 参数是用来查看适用客户端 outbounds JSON 的，仅供测试使用

用法：xray genc [name]

举例：

xray gen
xray gen tcp

提醒，你也可以使用 xray client ，跟 genc 作用是一样的。

bbr
bbr 参数是启用 BBR 优化的

使用: xray bbr

bin
bin 参数是直接调用 Xray 核心运行相关命令，此参数可完全兼容所有 Xray 命令

用法：xray bin [...]

举例：xray bin help

默认兼容的命令：api, x25519, tls, run, uuid

举例：xray x25519

xapi
xapi 参数类似 xray api, 但 API 后端使用当前运行的 Xray 服务

用法：xray xapi [...]

举例：xray xapi statsquery

fix-config.json
fix-config.json 参数是用来修复 config.json 文件的

使用: xray fix-config.json

update
update 参数是用来更新的

用法：xray update [core | sh | caddy] [ver]

举例:

xray update -> 更新核心
xray update core -> 更新核心
xray update core v1.8.3 -> 更新核心，使用 v1.8.3 版本
xray update sh -> 更新脚本
xray update caddy -> 更新 Caddy

log
log 参数是用来查看 Xray 运行的实时日志

使用：xray log

status
status 是查看运行状态的参数

使用：xray status

start, stop, restart
start, stop, restart 是管理 Xray 启动，停止，重启 的参数

用法：xray [start | stop | restart] [caddy]

举例：

xray restart -> 重启 Xray
xray restart caddy -> 重启 Caddy

reinstall
reinstall 是重装脚本的参数

使用: xray reinstall

uninstall
uninstall 是卸载脚本的参数

使用：xray uninstall

中转
如果你需要使用 A 机器转发流量到 B 机器

那么请看：Xray 脚本中转教程

帮助
哎呀，不想写了，其他的一些参数用法，请查看帮助

使用：xray help

目录
Xray 脚本全部身家保存在 /etc/xray

脚本：/etc/xray/sh
核心：/etc/xray/bin
配置：/etc/xray/conf

不要为什么不符合 XXX 规则，因为我更想符合一键删除理念。

友情提醒
如果你添加了 *TLS 协议的配置，请务必设置伪装网站，使用 xray web tls 快速设置伪装网站

伪装网站
伪装网站是一个反代，指的是打开自己域名的时候显示来自伪装网站的内容

自动 TLS 说明
Xray 脚本自动 TLS 帮助说明

备份脚本
考虑到可能会有不可描述的事情发生，你可以将 Xray 脚本备份一下以防止万一。

Github 地址：https://github.com/233boy/Xray

你可以 Fork 一份，如果本人一键删库跑路了，你也可以照样正常安装使用

安装命令如下：

wget https://github.com/233boy/Xray/archive/main.tar.gz -O Xray-main.tar.gz;tar -zxvf Xray-main.tar.gz;cd Xray-main;chmod +x i*;./i* -l
记得要把安装命令中的 233boy 更改成你的 Github 用户名

关注我们
Telegram 频道：https://t.me/tg2333

Telegram 群组：https://t.me/tg233boy

反馈问题
https://github.com/233boy/xray/issues
