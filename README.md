# Django-MYSQL-to-make-easy-API
create sql first or the project will start failed.

you can learn more from

https://www.cnblogs.com/ashenweb/p/14008651.html

# create sql

drop database if exists bbs;
create database bbs default charset utf8 collate utf8_general_ci;
use bbs;

drop table if exists t_user;
drop table if exists t_content;
drop table if exists t_content2;

create table t_user(
    id int(10) primary key auto_increment,
    name varchar(20) not null,
    password varchar(64) default null,
    email varchar(64) default null
);

insert into t_user(name,password,email) values('user1','123','123456@qq.com');
insert into t_user(name,password,email) values('user2','123','123456@gmail.com');





create table t_content(
    id int(10) primary key auto_increment,
    title varchar(20) not null,
    content varchar(64) default null
);
insert into t_content(title,content) values('title1','content1');
insert into t_content(title,content) values('title2','content2');


create table t_content2(
    id int(10) primary key auto_increment,
    _id2 int(10) not null,
    reply varchar(64) not null
);
insert into t_content2(_id2,reply) values(1,'reply1');
insert into t_content2(_id2,reply) values(1,'reply2');
