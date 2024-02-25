First commit fff--drop database gamebook_test;
create database gamebook_test;
use gamebook_test;
create table gamebook_test.game (
    id int(10) unsigned auto_increment,
    title varchar(50),
    image_path varchar(255),
    genre_code varchar(255),
    primary key (id)
);

create table gamebook_test.user (
    id int(10) unsigned auto_increment,
    username varchar(50),
    primary key (id)
);

create table gamebook_test.rating (
    user_id int(10) unsigned,
    game_id int(10) unsigned,
    score tinyint(1),
    primary key (user_id, game_id)
);

insert into gamebook_test.user values(1, 'Dan');
insert into gamebook_test.game (title, image_path, genre_code) values('Game 1 - Duke Nukem', 'images/game1.png', 'shooter');
insert into gamebook_test.game (title, image_path, genre_code) values('Game 2 - Mortal Kombat', 'images/game2.png', 'shooter');
insert into gamebook_test.game (title, image_path, genre_code) values('Game 3 - Assassin\'s Creed', 'images/game3.png', 'shooter');
insert into gamebook_test.game (title, image_path, genre_code) values('Game 4 - Legend of Zelda', 'images/game4.png', 'adventure');
insert into gamebook_test.game (title, image_path, genre_code) values('Game 5 - Fallout', 'images/game5.png', 'zombies');
insert into gamebook_test.game (title, image_path, genre_code) values('Game 6 - Mario Brothers', 'images/game6.png', 'jumping');
insert into gamebook_test.rating values(1,1,5);

select * from game

