# comandos-mysql
manual de comandos mysql

## script de segurança
mysql_secure_installation

## ver base de dados
```
SHOW DATABASES;
```

## criar nova base de dados
```
CREATE DATABASE <name>;
```

## criar novo utilizador localhost
```
CREATE USER 'newuser'@'localhost' IDENTIFIED BY 'password';
```

## criar novo utilizador web
```
CREATE USER 'newuser'@'%' IDENTIFIED BY 'password';
```

## alterar passsword
```
ALTER USER 'root'@'localhost' IDENTIFIED BY 'newPass';
```

## todas as permissoes
```
GRANT ALL PRIVILEGES ON *.* TO 'newuser'@'localhost';
```

## reload all the privileges.
```
FLUSH PRIVILEGES;
```

## Grant Different User Permissions

* ALL PRIVILEGES- as we saw previously, this would allow a MySQL user full access to a designated database (or if no database is selected, global access across the system)
* CREATE- allows them to create new tables or databases
* DROP- allows them to them to delete tables or databases
* DELETE- allows them to delete rows from tables
* INSERT- allows them to insert rows into tables
* SELECT- allows them to use the SELECT command to read through databases
* UPDATE- allow them to update table rows
* GRANT OPTION- allows them to grant or remove other users’ privileges

## specific user with a permission
```
GRANT type_of_permission ON database_name.table_name TO 'username'@'localhost';
```

## revoke a permission
```
REVOKE type_of_permission ON database_name.table_name FROM 'username'@'localhost';
```

## see current permissions
```
SHOW GRANTS FOR 'username'@'localhost';
```

## delete databases with DROP and users
```
DROP USER 'username'@'localhost';
DROP DATABASE <name>;
