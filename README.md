# expect_auto_login
linux shell利用expect 自动ssh登录
脚本中,
loginpass 后面是ssh 登录的密码

## 环境要求/前置条件
操作系统必须是linux或类Unix系统
要求安装了expect

## centos 安装expect
mkdir expect
cd expect
wget http://prdownloads.sourceforge.net/tcl/tcl8.5.19-src.tar.gz
tar xf tcl8.5.19-src.tar.gz
cd tcl8.5.19
cd unix
./configure
make
make install

wget http://nchc.dl.sourceforge.net/project/expect/Expect/5.45/expect5.45.tar.gz
tar xf expect5.45.tar.gz
cd expect5.45
./configure --with-tcl=/usr/local/lib/ --with-tclinclude=/opt/software/expect/tcl8.5.19/generic/
make
make install
