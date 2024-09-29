# Week 4
## Exercises 4: Join
### 1  
select country.name as "country name", airport.name as "airport name"  
from airport  
inner join country on airport.iso_country = country.iso_country  
where airport.iso_country = 'FI'  
and scheduled_service = 'yes';

![Ảnh chụp màn hình 2024-09-29 040907](https://github.com/user-attachments/assets/c91d38dc-a83d-4fa0-b3a6-30a2b220fda5)

### 2   
select game.screen_name, airport.name  
from game  
inner join airport on game.location = airport.ident;

![Ảnh chụp màn hình 2024-09-29 041431](https://github.com/user-attachments/assets/c4319e3b-ae13-4cde-82a4-806b7e965ce8)


### 3  
select game.screen_name, country.name  
from game  
inner join airport on game.location = airport.ident  
inner join country on airport.iso_country = country.iso_country;

![Ảnh chụp màn hình 2024-09-29 041634](https://github.com/user-attachments/assets/1469f2bb-6194-48ab-91e0-e854d42b575c)


### 4 
select airport.name, game.screen_name  
from airport  
left join game on game.location = airport.ident  
where airport.name like "%Hels%";  

![Ảnh chụp màn hình 2024-09-29 042701](https://github.com/user-attachments/assets/8f7c2546-91b1-44c8-9736-6866af32aae0)


### 5  
select goal.name, game.screen_name  
from goal  
left join goal_reached on goal_reached.goal_id = goal.id  
left join game on goal_reached.game_id = game.id;

![Ảnh chụp màn hình 2024-09-29 044011](https://github.com/user-attachments/assets/7021eb82-b785-4fef-9567-632e7f74102d)
