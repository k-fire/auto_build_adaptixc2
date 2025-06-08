# auto_build_adaptixc2

自动编译服务端，降低glibc版本要求

ldd (Debian GLIBC 2.28-10+deb10u3) 2.28

windows客户端为静态编译，没有乱七八糟的依赖，修改配置文件路径为同目录下

由于agent在服务端编译，确保服务端运行环境满足以下依赖

```
sudo apt install golang-1.23 mingw-w64 make
sudo ln -s /usr/lib/go-1.23/bin/go /usr/local/bin/go

// curl -LO https://go.dev/dl/go1.24.3.linux-amd64.tar.gz
// tar -C /usr/local -xzf go1.24.3.linux-amd64.tar.gz
// echo "export PATH=$PATH:/usr/local/go/bin" >> /etc/profile
// export PATH=$PATH:/usr/local/go/bin
// go version
// go env -w  GOPROXY=https://goproxy.cn,direct
```
而且要求传输速度，否则客户端生成时容易超时

#

Automatically compile the server and lower the glibc version requirement

ldd (Debian GLIBC 2.28-10+deb10u3) 2.28

The windows client is statically compiled, without messy dependencies, and the configuration file path is changed to the same directory
