这个用于创建可以运行docker和go的VM。

需要注意的是vagrantfile里最后的step似乎没有成功写入到~/.profile，如果是这样的话需要手动写入下。

check if ~/.profile contains below:

export GOROOT=/usr/local/go
export PATH=$PATH:/usr/local/go/bin:$GOPATH/bin
export GOPATH=$HOME/goproject

IF NOT, RUN:
   echo 'export GOROOT=/usr/local/go' >> ~/.profile
   echo 'export PATH=$PATH:/usr/local/go/bin:$GOPATH/bin' >> ~/.profile
   echo 'export GOPATH=$HOME/goproject' >> ~/.profile