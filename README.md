# php_snowflake


## What is php_snowflake?

[Twitter SnowFlake](https://github.com/twitter/snowflake) PHP version of the algorithm

## Description

### ZTS
```
0 2　　　　　　    15　　　　　　20　 28　　　   32
--+----------------+--------------+----+----------+
 00|timestamp(ms)  | service_num| pid | sequence     |
--+----------------+--------------+----+----------+
```

### NTS
```
0 2　　　　　　    15　　　　　　20　 28　　　   32
--+----------------+--------------+----+----------+
 00|timestamp(ms)  | service_num| tid | sequence     |
--+----------------+--------------+----+----------+
```

## Installation
```
./configure --with-php-config=/you/path
make
make install
```
## Example
```
$service_num = 999;
for ($i=0; $i < 10; $i++) { 
        echo PhpSnowFlake::nextId($service_num)."\n";
}
/*
00146523488416500999000634280001
00146523488416500999000634280002
00146523488416500999000634280003
00146523488416500999000634280004
00146523488416500999000634280005
00146523488416600999000634280001
00146523488416600999000634280002
00146523488416600999000634280003
00146523488416600999000634280004
00146523488416600999000634280005
*/
```
## License
Copyright (c) 2016 by [Towers](http://zheng-ji.info) released under MIT License.


