Memcache是放在内存中的

源生代码：（先在php.net中查php安装memcached扩展）
$memcache= new Memcached;
$memcache->addServers('域名','端口');
$memcache->setOptions('要配置的参数');
然后利用memcache的set get delect flush进行“存取清”


（安装是关键）
Redis其实就是一个简单的数据库,断电可恢复
 $redis  = new \Redis;
 $redis->connet($options['host'], $options['port']) :
 $redis->connet($options['host'], $options['port'], $options['timeout']);
然后利用Redis的set get delect flushDb进行“存取清”



thinkphp F方法只能用于缓存简单数据类型在文件中，不支持有效期和缓存对象
