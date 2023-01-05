# db 생성

create database db02;

CREATE TABLE `db01`.`user` (
`userNo` INT NOT NULL AUTO_INCREMENT,
`name` VARCHAR(45) NULL,
`id` VARCHAR(45) NULL,
`pw` VARCHAR(45) NULL,
PRIMARY KEY (`userNo`),
UNIQUE INDEX (id));
  
CREATE TABLE `db01`.`board` (
`boardNo` INT NOT NULL AUTO_INCREMENT,
`userNo` INT NOT NULL,
`title` VARCHAR(45) NULL,
`contents` VARCHAR(1024) NULL,
`date` DATETIME NULL ,
PRIMARY KEY (`boardNo`));

CREATE TABLE `db01`.`comment` (
`commentNo` INT NOT NULL AUTO_INCREMENT,
`boardNo` INT NOT NULL,
`userNo` INT NOT NULL,
`comment` VARCHAR(45) NULL,
`date` DATETIME NULL,
PRIMARY KEY (`commentNo`));
