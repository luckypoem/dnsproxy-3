# dnsproxy
Proxy DNS query use TCP in php <br />
一个使用php通过tcp协议从远程dns服务器获取真实ip的小工具 <br />
程序要求
- Linux: root用户,且有独立ip,不然无法监听53端口(未测试，无独立ip主机，无root权限主机，求赞助)
- Windows: 管理员用户，且有独立ip，不然无法监听53端口（已测试，测试机型为Win10 Pro x64）
- 无独立ip也可使用，但不能在公网对外提供解析服务

已实现的功能有
- 使用tcp协议从远程服务器获取dns

打算实现但还未实现的有
- dns缓存功能
- 后台管理功能
- 其实很想做自动抓取SmartHosts中纯净ip地址功能的，怕有关部门约谈，这个功能还是算了吧

说明
- 默认使用tcp协议53端口的8.8.8.8
- 若需修改上游dns服务器，可直接修改8.8.8.8为你需要的上游服务器
- 若需修改上游dns服务器端口，可直接修改53为你需要的端口
- 若需要修改协议为udp，直接取消13、15行注释，注释掉14、16行
- 可CLI模式运行，直接"php index.php"即可(windows已测试)
- 可web运行，访问index.php，然后关掉浏览器即可(未测试)
- 使用时需在用户电脑上设置dns地址为你服务器地址
- index.php可修改为你喜欢的名字
