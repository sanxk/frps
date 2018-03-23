# [common]是不可或缺的部分
[common]
bind_addr = 193.112.138.86
bind_port = 7000

# UDP端口，以帮助使UDP孔穿透NAT
bind_udp_port = 7001

# 用于kcp协议的udp端口，它可以与'bind_port'相同
# #如果未设置，kcp将在frps中禁用
kcp_bind_port = 7000

# 指定哪个地址代理将侦听，默认值与bind_addr相同
# proxy_bind_addr = 127.0.0.1

# 如果你想支持虚拟主机，你必须设置HTTP端口进行监听（可选）
vhost_http_port = 80
vhost_https_port = 443

# 设置dashboard_addr和dashboard_port以查看frps的仪表板
# dashboard_addr的默认值是相同与bind_addr
# 仅当设置了dashboard_port时，仪表板才可用
dashboard_addr = 0.0.0.0
dashboard_port = 7500

# 为基本身份验证面板用户和pwd保护，如果没有设置，包括默认值为admin
dashboard_user = sanxk
dashboard_pwd = 141223

# 自v0.10.0以来，privilege_token是唯一受支持的模式
privilege_token = 12345678

# 心跳配置，不建议修改默认值
# heartbeat_timeout的默认值是90
# heartbeat_timeout = 90

# 只允许frpc绑定您列出的端口，如果您不设置任何内容，则不会有任何限制
privilege_allow_ports = 2000-3000,3001,3003,4000-50000

# 在每个代理pool_count将变更为max_pool_count如果他们超过最大值
max_pool_count = 5

# 每个客户端可以使用个最大端口，默认值为0表示没有限制
max_ports_per_client = 0

# authentication_timeout装置的超时间隔（秒），当连接FRPC FRPS
# 如果authentication_timeout为零，则时间未验证，默认值为900s
authentication_timeout = 900

# 如果subdomain_host不为空，则可以在frpc的配置文件中键入http或https时设置子域
# 当子域测试时，路由使用的主机是test.frps.com
# subdomain_host = frps.com

# 如果使用tcp流复用，默认值为true
tcp_mux = true
