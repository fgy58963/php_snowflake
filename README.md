# php_snowflake


## What is php_snowflake?

[Twitter SnowFlake](https://github.com/twitter/snowflake) PHP version of the algorithm

## Requires
PHP >= 7.0

## Description

### ZTS
```
0　　　　　　    13　　　　18　  28　　　    32
+----------------+--------------+----+----------+
 |timestamp(ms)  | service_no | pid | sequence   |
+----------------+--------------+----+----------+
```

### NTS
```
0　　　　　　    13　　　 　18　  28　　　    32
+----------------+--------------+----+----------+
|timestamp(ms)  | service_no | tid | sequence   |
+----------------+--------------+----+----------+
```

## Installation
```
phpize
./configure --with-php-config=/you/phppath/php-config
make
make install
```
## Example
```
$service_no = 999;
for ($i=0; $i < 10; $i++) { 
        echo PhpSnowFlake::nextId($service_no)."\n";
}
/*
14652348841650099900000634280001
14652348841650099900000634280002
14652348841650099900000634280003
14652348841650099900000634280004
14652348841650099900000634280005
14652348841660099900000634280001
14652348841660099900000634280002
14652348841660099900000634280003
14652348841660099900000634280004
14652348841660099900000634280005
*/
```
## License
Copyright (c) 2016 by [Towers](http://zheng-ji.info) released under MIT License.


