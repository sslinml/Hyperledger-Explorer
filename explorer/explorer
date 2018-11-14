# Hyperledger-Explorer

fabric-explorer能查看到区块的信息，比如交易、区块、节点，部署的链码情况等，所以建议在网络搭建成功之后，可以尝试部署一下fabric-explorer。

一.下载支持mysql版本的fabric-explorer（目前支持的数据库有mysql和postgre，因为本机有mysql环境所以安装mysql的版本）<br>
```
1.git clone https://github.com/hyperledger/blockchain-explorer.git
2.cd blockchain-explorer
3.git checkout reactbranch
```
二.Database setup 配置数据库，基于路径目录 `db/fabricexplorer.sql`
```
1.mysql -u root -p < db/fabricexplorer.sql
```

三.启动网络
```
1. cd first-network
2. ./bootstrap-1.0.2.sh    //This is going to download the necessary　binaries and hyperledger docker images.
3. mkdir -p ./channel-artifacts     //由于Hyperleger Explorer中的first-network中没有channel-artifacts文件夹，需要创建
4. ./byfn.sh -m generate -c mychannel
5. ./byfn.sh -m up -c mychannel
```
四.启动浏览器
```
1. cd blockchain-explorer
2. Modify config.json to update one of the channel 
   * mysql host, username, password details
 json
 "channel": "mychannel",
 "mysql":{
      "host":"127.0.0.1",
      "database":"fabricexplorer",
      "username":"root",
      "passwd":"123456"
   }
```
注意network-config中一些配置的路径是否对，默认不需要更改，如果替换网络，需要更改！
```
3. npm install    //根据package.jason文件生成JDK的相关依赖包
4. ./start.sh    //里面有一句node main.js >log.log 2>&1 &，意思是执行结果信息打印在了项目的log.log文件中，终端不显示任何信息
可以改为node main.js
```
Finally:Launch the URL http://localhost:8080 on a browser.




