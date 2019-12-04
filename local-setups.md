Setting up servers for local use
---

Warning
---
The steps below are for local setup only. This removes the security features of
specific products and would prevent any attacker to access your system. Tread
with care.

AppArmor
---


MySQL 8.0
---
1. Add mysql to disabled apparmor profiles
2. To allow remote access from root to your mysql instance do the following:
  * add `bind-address = 0.0.0.0` to your mysqld config
  * create a new 'root' user for remote
    ```sql
      > -- add "remote root"
      > CREATE USER 'root'@'%' [IDENTIFIER BY 'password']
      > -- grant all privileges possible
      > GRANT ALL PRIVILEGES ON *.* TO 'root'@'%' [WITH GRANT OPTION]

    ```
