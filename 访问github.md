cmd
set HTTPS_PROXY=socks5://127.0.0.1:10808 
set HTTP_PROXY=socks5://127.0.0.1:10808 

shell
export HTTPS_PROXY=socks5://127.0.0.1:1080
export HTTP_PROXY=socks5://127.0.0.1:1080



export PATH=/opt/homebrew/bin:$PATH


mongodb安装地址：
/opt/homebrew/Cellar/mongodb-community/7.0.2/

启动命令：
brew services start mongodb/brew/mongodb-community

| Intel Processor | Apple Silicon Processor |  |
| ---- | ---- | ---- |
| [configuration file](https://www.mongodb.com/docs/manual/reference/configuration-options/) | `/usr/local/etc/mongod.conf` | `/opt/homebrew/etc/mongod.conf` |
| [`log directory`](https://www.mongodb.com/docs/manual/reference/configuration-options/#mongodb-setting-systemLog.path) | `/usr/local/var/log/mongodb` | `/opt/homebrew/var/log/mongodb` |
| [`data directory`](https://www.mongodb.com/docs/manual/reference/configuration-options/#mongodb-setting-storage.dbPath) | `/usr/local/var/mongodb` | `/opt/homebrew/var/mongodb` |
