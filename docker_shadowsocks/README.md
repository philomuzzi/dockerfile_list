编译方法
---
>
1. docker build -t philomuzzi/docker_shadowsocks-libev:v1.4.8 docker_shadowsocks/
2. 进入系统sysctl --system
3. docker commit -m "update optimized info" -a "philomuzzi" 容器ID philomuzzi/docker_shadowsocks-libev:tags

使用方法
---
>
docker run -d -p [port]:[port] philomuzzi/shadowsocks-libev:tags -s 0.0.0.0 -p [port] -k [password] -m aes-256-cfb

参数说明
---
>      -s <server_host>           host name or ip address of your remote server
>      -p <server_port>           port number of your remote server
>      -l <local_port>            port number of your local server
>      -k <password>              password of your remote server
>
>
>      [-m <encrypt_method>]      encrypt method: table, rc4, rc4-md5
>                                 aes-128-cfb, aes-192-cfb, aes-256-cfb,
>                                 bf-cfb, camellia-128-cfb, camellia-192-cfb,
>                                 camellia-256-cfb, cast5-cfb, des-cfb,
>                                 idea-cfb, rc2-cfb and seed-cfb
>      [-f <pid_file>]            file to store the pid
>      [-t <timeout>]             socket timeout in seconds
>      [-c <config_file>]         config file in json
>
>
>      [-i <interface>]           network interface to bind,
>                                 not available in redir mode
>      [-b <local_address>]       local address to bind,
>                                 not available in server mode
>      [-u]                       enable udprelay mode
>                                 not available in redir mode
>      [-L <addr>:<port>]         setup a local port forwarding tunnel,
>                                 only available in tunnel mode
>      [-v]                       verbose mode
>
>
>      [--fast-open]              enable TCP fast open,
>                                 only available on Linux kernel > 3.7.0
>      [--acl <acl_file>]         config file of ACL (Access Control List)