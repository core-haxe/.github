_Note: all these repos are currently considered "work in progress"_

<h4>Database</h4>



- [__db-core__](https://github.com/core-haxe/db-core) - pluggable database abstraction
  - [__db-sqlite__](https://github.com/core-haxe/db-sqlite) - sqlite database plugin for [__db-core__](https://github.com/core-haxe/db-core)
    - [__sqlite3__](https://github.com/core-haxe/sqlite3) - sqlite3 for all relevant haxe targets
      - [__libsqlite3__](https://github.com/core-haxe/libsqlite3) - sqlite3 externs for hxcpp
  - [__db-mysql__](https://github.com/core-haxe/db-mysql) - mysql database plugin for [__db-core__](https://github.com/core-haxe/db-core)
    - [__mysql__](https://github.com/core-haxe/mysql) - mysql for all relevant haxe targets
- [__entities__](https://github.com/core-haxe/entities) - entity database system for ORM

<h4>Communication</h4>

- [__http__](https://github.com/core-haxe/http) - flexible http client supporting different http providers
- [__rest__](https://github.com/core-haxe/rest) - rest client supporting fully typed rest operations

<h4>Messaging</h4>

- [__queues-core__](https://github.com/core-haxe/queues-core) - pluggable queue abstraction
  - [__queues-rabbitmq__](https://github.com/core-haxe/queues-rabbitmq) - rabbitmq queue plugin for [__queues-core__](https://github.com/core-haxe/queues-core)
    - [__rabbitmq__](https://github.com/core-haxe/rabbitmq) - rabbitmq for all relevant haxe targets
- [__json-rpc__](https://github.com/core-haxe/json-rpc) - json rpc client supporting fully typed rest operations

<h4>Services</h4>

- __services-core__ - SOA style framework

<h4>Misc</h4>

- [__libgit2__](https://github.com/core-haxe/libgit2) - libgit2 externs for hxcpp

<h4>Utilities</h4>

- [__logging__](https://github.com/core-haxe/logging) - flexible logging framework supporting various "adaptors"
- [__promises__](https://github.com/core-haxe/promises) - promise lib (literally a typedef for thenshim currently)

---

<details>
  <summary>Builld Status</summary>
  <br/>
  
  | Repository | Builld Status |
  |---------|--------|
  | [__db-core__](https://github.com/core-haxe/db-core) | <a href="https://github.com/core-haxe/db-core/actions/workflows/nodejs.yaml"><img src="https://github.com/core-haxe/db-core/actions/workflows/nodejs.yaml/badge.svg">&nbsp;<a href="https://github.com/core-haxe/db-core/actions/workflows/hl.yaml"><img src="https://github.com/core-haxe/db-core/actions/workflows/hl.yaml/badge.svg">&nbsp;<a href="https://github.com/core-haxe/db-core/actions/workflows/hxcpp.yaml"><img src="https://github.com/core-haxe/db-core/actions/workflows/hxcpp.yaml/badge.svg">&nbsp;<a href="https://github.com/core-haxe/db-core/actions/workflows/neko.yaml"><img src="https://github.com/core-haxe/db-core/actions/workflows/neko.yaml/badge.svg"> |
  | [__sqlite3__](https://github.com/core-haxe/sqlite3) | <a href="https://github.com/core-haxe/sqlite3/actions/workflows/nodejs.yaml"><img src="https://github.com/core-haxe/sqlite3/actions/workflows/nodejs.yaml/badge.svg">&nbsp;<a href="https://github.com/core-haxe/sqlite3/actions/workflows/hl.yaml"><img src="https://github.com/core-haxe/sqlite3/actions/workflows/hl.yaml/badge.svg">&nbsp;<a href="https://github.com/core-haxe/sqlite3/actions/workflows/hxcpp.yaml"><img src="https://github.com/core-haxe/sqlite3/actions/workflows/hxcpp.yaml/badge.svg">&nbsp;<a href="https://github.com/core-haxe/sqlite3/actions/workflows/neko.yaml"><img src="https://github.com/core-haxe/sqlite3/actions/workflows/neko.yaml/badge.svg"> |
  | [__libsqlite3__](https://github.com/core-haxe/libsqlite3) | <a href="https://github.com/core-haxe/libsqlite3/actions/workflows/windows.yaml"><img src="https://github.com/core-haxe/libsqlite3/actions/workflows/windows.yaml/badge.svg">&nbsp;<a href="https://github.com/core-haxe/libsqlite3/actions/workflows/ubuntu.yaml"><img src="https://github.com/core-haxe/libsqlite3/actions/workflows/ubuntu.yaml/badge.svg">&nbsp;<a href="https://github.com/core-haxe/libsqlite3/actions/workflows/mac.yaml"><img src="https://github.com/core-haxe/libsqlite3/actions/workflows/mac.yaml/badge.svg"> |
  | [__entities__](https://github.com/core-haxe/entities) | <a href="https://github.com/core-haxe/entities/actions/workflows/nodejs.yaml"><img src="https://github.com/core-haxe/entities/actions/workflows/nodejs.yaml/badge.svg">&nbsp;<a href="https://github.com/core-haxe/entities/actions/workflows/hl.yaml"><img src="https://github.com/core-haxe/entities/actions/workflows/hl.yaml/badge.svg">&nbsp;<a href="https://github.com/core-haxe/entities/actions/workflows/hxcpp.yaml"><img src="https://github.com/core-haxe/entities/actions/workflows/hxcpp.yaml/badge.svg">&nbsp;<a href="https://github.com/core-haxe/entities/actions/workflows/neko.yaml"><img src="https://github.com/core-haxe/entities/actions/workflows/neko.yaml/badge.svg"> |
  | [__http__](https://github.com/core-haxe/http) | <a href="https://github.com/core-haxe/http/actions/workflows/nodejs.yaml"><img src="https://github.com/core-haxe/http/actions/workflows/nodejs.yaml/badge.svg">&nbsp;<a href="https://github.com/core-haxe/http/actions/workflows/hl.yaml"><img src="https://github.com/core-haxe/http/actions/workflows/hl.yaml/badge.svg">&nbsp;<a href="https://github.com/core-haxe/http/actions/workflows/hxcpp.yaml"><img src="https://github.com/core-haxe/http/actions/workflows/hxcpp.yaml/badge.svg">&nbsp;<a href="https://github.com/core-haxe/http/actions/workflows/neko.yaml"><img src="https://github.com/core-haxe/http/actions/workflows/neko.yaml/badge.svg"> |
  | [__rest__](https://github.com/core-haxe/rest) | <a href="https://github.com/core-haxe/rest/actions/workflows/nodejs.yaml"><img src="https://github.com/core-haxe/rest/actions/workflows/nodejs.yaml/badge.svg">&nbsp;<a href="https://github.com/core-haxe/rest/actions/workflows/hl.yaml"><img src="https://github.com/core-haxe/rest/actions/workflows/hl.yaml/badge.svg">&nbsp;<a href="https://github.com/core-haxe/rest/actions/workflows/hxcpp.yaml"><img src="https://github.com/core-haxe/rest/actions/workflows/hxcpp.yaml/badge.svg">&nbsp;<a href="https://github.com/core-haxe/rest/actions/workflows/neko.yaml"><img src="https://github.com/core-haxe/rest/actions/workflows/neko.yaml/badge.svg"> |

</details>
