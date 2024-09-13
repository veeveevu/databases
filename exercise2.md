#1
select * from goal;
#2
select name, type from airport where iso_country like "FI";
#3
select name from airport where iso_country like "FI" order by name asc;
#4
select name, type from airport where iso_country like "FI" order by type asc, name asc;
#5
select name from country where name like "F%";
#6
select name from country where name like "%F%";
#7
select location from game where screen_name like "Vesa";
#8
select co2_consumed from game where screen_name like "Ilkka";
#9
select distinct co2_budget from game;
#10
alter table game add column co2_left int;
update game set co2_left = co2_budget - co2_consumed;
select screen_name, co2_budget, co2_consumed, co2_left
from game where screen_name like "Ilkka";
