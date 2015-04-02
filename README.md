1. Step by step guide for mysql and elastic search connectivity (https://github.com/jprante/elasticsearch-river-jdbc/wiki/Quickstart)
2. download elastic search version 1.0 from elastic search site (elasticsearch-1.0.0.RC1)
3. download my sql java connector from (http://cdn.mysql.com/Downloads/Connector-J/mysql-connector-java-gpl-5.1.35.msi)
4. river jdbc driver is from (http://bit.ly/1dKqNJy)
5. all the above jars are compatible with v1.0 of elastic search and mysql 5.1 and river jdbc
6. start insert from mysql to elastic search (curl -XPUT 'localhost:9200/_river/my_jdbc_driver/_meta' -d '{"type" : "jdbc", "jdbc" : {"url" :"jdbc:mysql://localhost:3306/World", "user" : "root", "password" : "ssutv123", "sql" : "select * from books_dummy1" }}')
7. use this command to query the data from elastic search (GET /jdbc/_search?pretty&q=young)
8. 
