# pymulticast
ues python to send or receive udp multicast

pymulticast -h

Usage:
  pymulticast receive MCAST_GRP MCAST_PORT [-i <ip>] [(-w <filepath> -t <split_time>)]
  pymulticast -h | --help
  pymulticast --version
  
Options:
  -h --help         显示帮助
  -i <ip>           指定监听网口, 默认为None, 即随机选取
  -w <filepath>     接收的数据写入到文件
  -t <split_time>   指定分片时间, 单位秒, 默认值为1800秒, 需要同时指定-w参数
  
Examples:
  pymulticast receive 239.1.1.1 1234
  pymulticast receive 239.1.1.1 1234 -i 192.168.11.48
  pymulticast receive 239.1.1.1 1234 -i 192.168.11.48 -w /mnt/data/local-disk1/record.ts -t 1800
