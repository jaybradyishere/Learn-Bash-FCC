camper: /project$ echo hello PostgreSQL
hello PostgreSQL
camper: /project$ psql --username=freecodecamp --dbname=postgres
LINE 2: CREATE DATABASE first_database;
postgres=> CREATE DATABASE first_database
postgres-> CREATE DATABASE first_database;
CREATE DATABASE second_database;
postgres=> \c second_database;
second_database=> \d
second_database=> CREATE TABLE first_table();
second_database=> \l
second_database=> CREATE TABLE second_table();
second_database=> \d
second_database=> \d second_table;
second_database=> ALTER TABLE second_table ADD COLUMN first_column INT;
second_database=> \d second_table
second_database=> ALTER TABLE second_table ADD COLUMN id INT;
second_database=> \d second_table;
second_database=> ALTER TABLE second_table ADD COLUMN age INT;
second_database=> \d second_table
ALTER TABLE second_table DROP COLUMN age;
second_database=> \d second_table
second_database-> ALTER TABLE second_table DROP COLUMN first_column;
second_database=> ALTER TABLE second_table ADD COLUMN name VARCHAR(30);
second_database=> \d second_table;
second_database=> ALTER TABLE second_table RENAME COLUMN name TO username;
second_database=> INSERT INTO second_table(id, username) VALUES(1, 'Samus');
second_database=> SELECT * FROM second_table;
second_database=> INSERT INTO second_table(id, username) VALUES(2, 'Mario');         
second_database=> SELECT * FROM second_table;
second_database=> DELETE FROM second_table WHERE username='Luigi';
second_database=> SELECT * FROM second_table;
second_database=> DELETE FROM second_table WHERE username='Mario';
second_database=> DELETE FROM second_table WHERE username='Samus';
second_database=> SELECT * FROM second_table;
second_database=> ALTER TABLE second_table DROP COLUMN username;
second_database=> ALTER TABLE second_table DROP COLUMN id;
second_database=> \l
second_database=> \d second_table
second_database=> DROP TABLE second_table;
second_database=> DROP TABLE first_table;
second_database=> \l
second_database=> ALTER DATABASE first_database RENAME TO mario_database;
second_database=> \l
second_database=> \c mario_database
mario_database=> DROP DATABASE second_database;
mario_database=> \d
mario_database=> CREATE TABLE characters();
mario_database=> ALTER TABLE characters ADD COLUMN character_id SERIAL;
mario_database=> \d
mario_database=> \d characters
mario_database=> ALTER TABLE characters ADD COLUMN name VARCHAR(30) NOT NULL;
mario_database=> ALTER TABLE characters ADD COLUMN homeland VARCHAR(60);
mario_database=> ALTER TABLE characters ADD COLUMN favorite_color VARCHAR(30);
mario_database=> \d characters
mario_database=> INSERT INTO characters(name, homeland, favorite_color) VALUES('Mario', 'Mushroom Kingdom', 'Red');     
mario_database=> SELECT * FROM characters;                                                                                     
mario_database=> INSERT INTO characters(name, homeland, favorite_color) VALUES('Luigi', 'Mushroom Kingdom', 'Green');
SELECT * FROM characters;
mario_database=> INSERT INTO characters(name, homeland, favorite_color) VALUES('Peach', 'Mushroom Kingdom', 'Pink');
