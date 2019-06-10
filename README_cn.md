### 说明
此仓库是基于[jwilder/nginx-proxy](https://github.com/jwilder/nginx-proxy)进行部分修改得来，用于nginx进行反向代理的

### 修改
此仓库的修改著需要参考于[Add support for path-based routing.](https://github.com/upstreamable/nginx-proxy/commit/b94e9a585a244748e754aa7641a189c8ba22e12f?diff=split)

增加修改的目的是为了增加一个可以配置nginx的location前缀的设置，基于[允许VIRTUAL_PATH路由（sub-VIRTUAL_HOST） ＃1083](https://github.com/jwilder/nginx-proxy/pull/1083)和[Implement rules for location / #1286](https://github.com/jwilder/nginx-proxy/issues/1286)

其中有人已经生成一个docker镜像[upstreamable/nginx-proxy
](https://hub.docker.com/r/upstreamable/nginx-proxy/tags),只不过里面的版本可以为18年的版本，所以自己重新构建一个

### 其他
通过修改nginx.tmpl实现可以代理静态文件，作为静态文件服务器[Adding the ability to serve static files #1037](https://github.com/jwilder/nginx-proxy/pull/1037)