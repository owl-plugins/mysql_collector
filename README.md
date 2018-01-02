# mysql_collector
owl 监控系统 mysql 采集插件，用于采集mysql的监控指标，并按照规定的格式返回。

# Metric 
| metric | tags | data_type | description | 
| ------ | ---- | ---- | ---- | 
| mysql.open_table | port | COUNTER |
| mysql.aborted_connects | port | COUNTER |
| mysql.bytes_received | port | COUNTER|
| mysql.com_begin | port | COUNTER |
| mysql.com_commit | port | COUNTER |
| mysql.com_delete | port | COUNTER |
| mysql.com_insert | port | COUNTER |
| mysql.com_rollback | port | COUNTER |
| mysql.com_select | port |  COUNTER |
| mysql.com_update | port  | COUNTER | 
| mysql.open_tables | port | GAUGE |
| mysql.questions | port  | COUNTER | 
| mysql.threads_connected | port | GAUGE |
| mysql.threads_running | port | GAUGE | 

```
# mkdir -p ~/gopath/src/github.com/owl-plugins/
# export GOPATH=~/gopath/src/github.com/owl-plugins/
# cd ~/gopath/src/github.com/owl-plugins/
# git clone https://github.com/owl-plugins/mysql_collector.git
# cd mysql_collector 
# go get ./... && go build
# ./mysql_collector --help
NAME:
   mysql_collector - mysql performance metric collector

USAGE:
   mysql_collector [global options] command [command options] [arguments...]

VERSION:
   0.1

AUTHOR:
   yingsong <wyingsong@163.com>

COMMANDS:
     help, h  Shows a list of commands or help for one command

GLOBAL OPTIONS:
   --host value      Connect to host. (default: "127.0.0.1") [$mysql_host]
   --user value      User for login if not current user (default: "root") [$mysql_user]
   --password value  Password to use when connecting to server. [$mysql_password]
   --port value      Port number to use for connection (default: 3306) [$mysql_port]
   --help, -h        show help
   --version, -v     print the version

COPYRIGHT:
   2011 (c) TalkingData.com
   ```
