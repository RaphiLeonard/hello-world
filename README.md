CREATE TABLE proxy
(id INTEGER PRIMARY KEY AUTOINCREMENT,
symbols TEXT,
number INTEGER,
relatednumber);

INSERT INTO proxy (symbols,number,relatednumber) VALUES ("a",1,23);
INSERT INTO proxy (symbols,number,relatednumber) VALUES ("s",19,50);
INSERT INTO proxy (symbols,number,relatednumber) VALUES ("d",4,19);
INSERT INTO proxy (symbols,number,relatednumber) VALUES ("f",6,0);
INSERT INTO proxy (symbols,number,relatednumber) VALUES ("g",7,53);
INSERT INTO proxy (symbols,number,relatednumber) VALUES ("h",8,100);

create table proxy2
(id INTEGER PRIMARY KEY AUTOINCREMENT,
symbols TEXT,
number INTEGER);

INSERT INTO proxy2 (symbols,number) VALUES ("a",1);
INSERT INTO proxy2 (symbols,number) VALUES ("b",2);
INSERT INTO proxy2 (symbols,number) VALUES ("c",3);
INSERT INTO proxy2 (symbols,number) VALUES ("d",4);
INSERT INTO proxy2 (symbols,number) VALUES ("e",5);
INSERT INTO proxy2 (symbols,number) VALUES ("f",6);
INSERT INTO proxy2 (symbols,number) VALUES ("g",7);
INSERT INTO proxy2 (symbols,number) VALUES ("h",8);

select proxy.symbols as letters,proxy.relatednumber as value_number from proxy join proxy2 on proxy2.number = proxy.number where relatednumber < 100;
