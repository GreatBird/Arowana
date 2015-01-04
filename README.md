Structuring Sinatra Web Application  

-----------------
#Precondition:  
1. bundle install  
2. check how to start the postgresql service in [c9.io](https://docs.c9.io/setting_up_postgresql.html)  
3. create sinatra_web DB  
```
postgres=# create database "sinatra_web";
```
  
4. create "user" table in postgresql DB  
```
CREATE TABLE "user" (
	id serial Primary key NOT NULL,
	username varchar(50) NOT NULL,
	pwd varchar(50) NOT NULL,
	permission varchar(10) NOT NULL
);
```
  
5. insert one record into user table  
```
INSERT INTO "user" (username, pwd, permission) VALUES ('admin', 'admin', 'rw');
```
  
#How to run the Application(on c9.io):  
```
$ rackup config.ru -p $PORT -o $IP  
```
  
Inspired from  
[Structuring Sinatra Applications](http://blog.sourcing.io/structuring-sinatra)  
[Structuring Sinatra Apps](http://graybike.co/2014/09/27/structuring-sinatra-apps-part-1/)  