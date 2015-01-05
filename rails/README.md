使用方法：
---

###生成
>docker build --no-cache=true -t="philomuzzi/rails:v1.0" .


###运行
>docker run -i -t --name rails -p [port]:[port] -v /root/xxx:/root/xxx philomuzzi/rails:v1.0 /bin/bash