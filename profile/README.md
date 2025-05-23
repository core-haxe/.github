_Note: all these repos are currently considered "work in progress"_

<h4>Database</h4>



- [__db-core__](https://github.com/core-haxe/db-core) - pluggable database abstraction
  - [__db-sqlite__](https://github.com/core-haxe/db-sqlite) - sqlite database plugin for [__db-core__](https://github.com/core-haxe/db-core)
    - [__sqlite3__](https://github.com/core-haxe/sqlite3) - sqlite3 for all relevant haxe targets
      - [__libsqlite3__](https://github.com/core-haxe/libsqlite3) - sqlite3 externs for hxcpp
  - [__db-mysql__](https://github.com/core-haxe/db-mysql) - mysql database plugin for [__db-core__](https://github.com/core-haxe/db-core)
    - [__mysql__](https://github.com/core-haxe/mysql) - mysql for all relevant haxe targets
      - [__libmysqlclient__](https://github.com/core-haxe/libmysqlclient) - mysqlclient externs for hxcpp
- [__entities2__](https://github.com/core-haxe/entities2) - entity database system for ORM

<h4>Communication</h4>

- [__http__](https://github.com/core-haxe/http) - flexible http client supporting different http providers
- [__rest__](https://github.com/core-haxe/rest) - rest client supporting fully typed rest operations
- [__ftp__](https://github.com/core-haxe/ftp) - (s)ftp client
- [__websockets__](https://github.com/core-haxe/websockets) - web socket client / server for all relevant haxe targets

<h4>Messaging</h4>

- [__queues-core__](https://github.com/core-haxe/queues-core) - pluggable queue abstraction
  - [__queues-rabbitmq__](https://github.com/core-haxe/queues-rabbitmq) - rabbitmq queue plugin for [__queues-core__](https://github.com/core-haxe/queues-core)
    - [__rabbitmq__](https://github.com/core-haxe/rabbitmq) - rabbitmq for all relevant haxe targets
      - [__php-amq-lib__](https://github.com/core-haxe/php-amq-lib) - php-amq-lib externs (rabbitmq for php target)
- [__json-rpc__](https://github.com/core-haxe/json-rpc) - json rpc client supporting fully typed rest operations

<h4>Misc</h4>

- [__libgit2__](https://github.com/core-haxe/libgit2) - libgit2 externs for hxcpp

<h4>Common</h4>

- [__serializers__](https://github.com/core-haxe/serializers) - serializers
- [__xml2object__](https://github.com/core-haxe/xml2object) - xml2object

<h4>Utilities</h4>

- [__logging__](https://github.com/core-haxe/logging) - flexible logging framework supporting various "adaptors"
- [__promises__](https://github.com/core-haxe/promises) - promise lib (literally a typedef for thenshim currently)
- [__haven__](https://github.com/core-haxe/haven) - build system

---

<details>
  <summary>Update / Install Scripts</summary><blockquote>
  <br/>
  
  <details>
    <summary>Windows (Batch)</summary><blockquote>
    <br/>
    
```    
@echo off

echo.
echo updating all core haxe libs
echo.

call :install_or_update_lib serializers, common

call :install_or_update_lib promises, utils
call :install_or_update_lib logging, utils
call :install_or_update_lib haven, utils

call :install_or_update_lib db-core, db
call :install_or_update_lib db-sqlite, db
call :install_or_update_lib sqlite3, db
call :install_or_update_lib libsqlite3, db
call :install_or_update_lib db-mysql, db
call :install_or_update_lib mysql, db
call :install_or_update_lib entities, db

call :install_or_update_lib http, comms
call :install_or_update_lib rest, comms
call :install_or_update_lib ftp, comms
call :install_or_update_lib websockets, comms

call :install_or_update_lib queues-core, messaging
call :install_or_update_lib queues-rabbitmq, messaging
call :install_or_update_lib rabbitmq, messaging
call :install_or_update_lib json-rpc, messaging

call :install_or_update_lib libgit2, misc

exit /B %ERRORLEVEL%

:install_or_update_lib
echo --------------------------------------------------------------------
echo core\%~1
echo --------------------------------------------------------------------
if exist %~2\%~1 (
  echo updating %~2\%~1  
  cd %~2\%~1
  git pull
  cd ..\..
) else (
  echo creating %~2\%~1
  if not exist "%~2" mkdir %~2
  cd %~2
  git clone https://github.com/core-haxe/%~1 && cd %~1
  haxelib dev %~1 .
  cd ..\..
)
echo.
exit /B 0
```

  </blockquote></details>  

  <details>
    <summary>Linux (Bash)</summary><blockquote>
    <br/>
    
```    
#!/bin/bash

echo
echo updating all core haxe libs
echo

install_or_update_lib() {
  echo "-------------------------------------------------------------------"
  echo "core/$1"
  echo "-------------------------------------------------------------------"
  if [ -d "$2/$1" ]
  then
    echo "updating $2/$1"
    cd $2/$1
    git pull
    cd ../..
  else
    echo "creating $2/$1"
    mkdir -p $2/$1
    cd $2
    git clone https://github.com/core-haxe/$1 && cd $1
    haxelib dev $1 .
    cd ../..
  fi  
  echo  
}

install_or_update_lib serializers common

install_or_update_lib promises utils
install_or_update_lib logging utils
install_or_update_lib haven utils

install_or_update_lib db-core db
install_or_update_lib db-sqlite db
install_or_update_lib sqlite3 db
install_or_update_lib libsqlite3 db
install_or_update_lib db-mysql db
install_or_update_lib mysql db
install_or_update_lib entities db

install_or_update_lib http comms
install_or_update_lib rest comms
install_or_update_lib ftp comms
install_or_update_lib websockets comms

install_or_update_lib queues-core messaging
install_or_update_lib queues-rabbitmq messaging
install_or_update_lib rabbitmq messaging
install_or_update_lib json-rpc messaging

install_or_update_lib libgit2 misc
```

  </blockquote></details>  
  
</blockquote></details>

---

<details>
  <summary>Build Status</summary>
  <br/>
  
  | Repository | Builld Status |
  |---------|--------|
  | [__db-core__](https://github.com/core-haxe/db-core) | <a href="https://github.com/core-haxe/db-core/actions/workflows/sqlite-nodejs.yaml"><img src="https://github.com/core-haxe/db-core/actions/workflows/sqlite-nodejs.yaml/badge.svg"></a>&nbsp;<a href="https://github.com/core-haxe/db-core/actions/workflows/sqlite-hxcpp.yaml"><img src="https://github.com/core-haxe/db-core/actions/workflows/sqlite-hxcpp.yaml/badge.svg"></a>&nbsp;<a href="https://github.com/core-haxe/db-core/actions/workflows/sqlite-hl.yaml"><img src="https://github.com/core-haxe/db-core/actions/workflows/sqlite-hl.yaml/badge.svg"></a>&nbsp;<a href="https://github.com/core-haxe/db-core/actions/workflows/sqlite-neko.yaml"><img src="https://github.com/core-haxe/db-core/actions/workflows/sqlite-neko.yaml/badge.svg"></a><br><a href="https://github.com/core-haxe/db-core/actions/workflows/mysql-nodejs.yaml"><img src="https://github.com/core-haxe/db-core/actions/workflows/mysql-nodejs.yaml/badge.svg"></a>&nbsp;<a href="https://github.com/core-haxe/db-core/actions/workflows/mysql-hxcpp.yaml"><img src="https://github.com/core-haxe/db-core/actions/workflows/mysql-hxcpp.yaml/badge.svg"></a> |
  | [__sqlite3__](https://github.com/core-haxe/sqlite3) | <a href="https://github.com/core-haxe/sqlite3/actions/workflows/nodejs.yaml"><img src="https://github.com/core-haxe/sqlite3/actions/workflows/nodejs.yaml/badge.svg"></a>&nbsp;<a href="https://github.com/core-haxe/sqlite3/actions/workflows/hl.yaml"><img src="https://github.com/core-haxe/sqlite3/actions/workflows/hl.yaml/badge.svg"></a>&nbsp;<a href="https://github.com/core-haxe/sqlite3/actions/workflows/hxcpp.yaml"><img src="https://github.com/core-haxe/sqlite3/actions/workflows/hxcpp.yaml/badge.svg"></a>&nbsp;<a href="https://github.com/core-haxe/sqlite3/actions/workflows/neko.yaml"><img src="https://github.com/core-haxe/sqlite3/actions/workflows/neko.yaml/badge.svg"></a> |
  | [__libsqlite3__](https://github.com/core-haxe/libsqlite3) | <a href="https://github.com/core-haxe/libsqlite3/actions/workflows/windows.yaml"><img src="https://github.com/core-haxe/libsqlite3/actions/workflows/windows.yaml/badge.svg"></a>&nbsp;<a href="https://github.com/core-haxe/libsqlite3/actions/workflows/ubuntu.yaml"><img src="https://github.com/core-haxe/libsqlite3/actions/workflows/ubuntu.yaml/badge.svg"></a>&nbsp;<a href="https://github.com/core-haxe/libsqlite3/actions/workflows/mac.yaml"><img src="https://github.com/core-haxe/libsqlite3/actions/workflows/mac.yaml/badge.svg"></a> |
  | [__entities__](https://github.com/core-haxe/entities) | <a href="https://github.com/core-haxe/entities/actions/workflows/sqlite-nodejs.yaml"><img src="https://github.com/core-haxe/entities/actions/workflows/sqlite-nodejs.yaml/badge.svg"></a>&nbsp;<a href="https://github.com/core-haxe/entities/actions/workflows/sqlite-hl.yaml"><img src="https://github.com/core-haxe/entities/actions/workflows/sqlite-hl.yaml/badge.svg"></a>&nbsp;<a href="https://github.com/core-haxe/entities/actions/workflows/sqlite-hxcpp.yaml"><img src="https://github.com/core-haxe/entities/actions/workflows/sqlite-hxcpp.yaml/badge.svg"></a>&nbsp;<a href="https://github.com/core-haxe/entities/actions/workflows/sqlite-neko.yaml"><img src="https://github.com/core-haxe/entities/actions/workflows/sqlite-neko.yaml/badge.svg"></a><br><a href="https://github.com/core-haxe/entities/actions/workflows/mysql-nodejs.yaml"><img src="https://github.com/core-haxe/entities/actions/workflows/mysql-nodejs.yaml/badge.svg"></a>&nbsp;<a href="https://github.com/core-haxe/entities/actions/workflows/mysql-hxcpp.yaml"><img src="https://github.com/core-haxe/entities/actions/workflows/mysql-hxcpp.yaml/badge.svg"></a> |
  | [__http__](https://github.com/core-haxe/http) | <a href="https://github.com/core-haxe/http/actions/workflows/nodejs.yaml"><img src="https://github.com/core-haxe/http/actions/workflows/nodejs.yaml/badge.svg"></a>&nbsp;<a href="https://github.com/core-haxe/http/actions/workflows/hl.yaml"><img src="https://github.com/core-haxe/http/actions/workflows/hl.yaml/badge.svg"></a>&nbsp;<a href="https://github.com/core-haxe/http/actions/workflows/hxcpp.yaml"><img src="https://github.com/core-haxe/http/actions/workflows/hxcpp.yaml/badge.svg"></a>&nbsp;<a href="https://github.com/core-haxe/http/actions/workflows/neko.yaml"><img src="https://github.com/core-haxe/http/actions/workflows/neko.yaml/badge.svg"></a> |
  | [__rest__](https://github.com/core-haxe/rest) | <a href="https://github.com/core-haxe/rest/actions/workflows/nodejs.yaml"><img src="https://github.com/core-haxe/rest/actions/workflows/nodejs.yaml/badge.svg"></a>&nbsp;<a href="https://github.com/core-haxe/rest/actions/workflows/hl.yaml"><img src="https://github.com/core-haxe/rest/actions/workflows/hl.yaml/badge.svg"></a>&nbsp;<a href="https://github.com/core-haxe/rest/actions/workflows/hxcpp.yaml"><img src="https://github.com/core-haxe/rest/actions/workflows/hxcpp.yaml/badge.svg"></a>&nbsp;<a href="https://github.com/core-haxe/rest/actions/workflows/neko.yaml"><img src="https://github.com/core-haxe/rest/actions/workflows/neko.yaml/badge.svg"></a> |

</details>
