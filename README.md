# Go
Go learning

> linux 安装 Go

- 到指定目录执行 
```
cd /usr/local/software/
wget https://dl.google.com/go/go1.10.3.linux-amd64.tar.gz
```

- 解压到/usr/local目录下
```
tar -C /usr/local -zxvf  go1.10.3.linux-amd64.tar.gz
```
- 添加/usr/local/go/bin目录到PATH变量中。添加到/etc/profile或$HOME/.profile

```
export GOROOT=/usr/local/go
export PATH=$PATH:$GOROOT/bin

//wq保存后source 一下
source /etc/profile
```

- go version 查看
```
root@FM:/usr/local/software# go version
go version go1.10.3 linux/amd64
```

- 执行src/fib/fib_test.go文件
```
root@FM:/home/Go/src/fib# go test -v -run TestFibList
=== RUN   TestFibList
1  1 2 3 5 8
--- PASS: TestFibList (0.00s)
PASS
ok      _/home/Go/src/fib       0.002s
```