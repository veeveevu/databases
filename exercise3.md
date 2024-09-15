# Week 3
## Exercises 3: Multiple Table Queries
### 1  
select country.name as "country name", airport.name as "airport name"  
from airport, country  
where airport.iso_country = country.iso_country  
and airport.iso_country = "IS";

![Ảnh chụp màn hình 2024-09-13 232213](https://github.com/user-attachments/assets/dd2ea10c-07b5-4834-97fd-915f3ae12773)

### 2   
select airport.name as "airport name"  
from airport  
where type = "large_airport"  
and airport.iso_country = "FR";

![Ảnh chụp màn hình 2024-09-13 232228](https://github.com/user-attachments/assets/71d0a9d3-6d53-4960-bcf5-57398af03213)

### 3  
select country.name as "country_name", airport.name as "airport_name"  
from country, airport  
where country.iso_country = airport.iso_country  
and country.continent = "AN";

![Ảnh chụp màn hình 2024-09-13 232317](https://github.com/user-attachments/assets/7be9549a-44e3-4d9f-b875-81ba5749a916)

### 4 
select elevation_ft  
from airport, game  
where game.screen_name = "Heini"  
and game.location = airport.ident;  
![Ảnh chụp màn hình 2024-09-13 232329](https://github.com/user-attachments/assets/a2010078-65dc-435b-bb26-f028b172c9f7)

### 5  
alter table airport add column elevation_m decimal(8,4);  
update airport set elevation_m = elevation_ft * 0.3048;  
select elevation_m  
from airport, game  
where screen_name = "Heini"  
and location = ident;

![Ảnh chụp màn hình 2024-09-13 232358](https://github.com/user-attachments/assets/da58487a-1c92-4e74-a00f-2a53885e307f)

### 6  
select airport.name  
from airport, game  
where screen_name = "Ilkka"  
and game.location = airport.ident;

![Ảnh chụp màn hình 2024-09-13 232409](https://github.com/user-attachments/assets/28292402-9d3b-42eb-8009-591617bbe02f)

### 7  
select country.name  
from country, airport, game  
where screen_name = "Ilkka"  
and game.location = airport.ident  
and airport.iso_country = country.iso_country;

![Ảnh chụp màn hình 2024-09-13 232420](https://github.com/user-attachments/assets/c2878400-cefc-4742-ae2f-4afb4e69d1c0)

### 8  
select goal.name  
from goal, game, goal_reached  
where game_id = game.id  
and goal_id = goal.id  
and screen_name = "Heini";

![Ảnh chụp màn hình 2024-09-13 232428](https://github.com/user-attachments/assets/f5e6f1e8-bfff-44e6-8668-a6ecdad0686f)

### 9  
select airport.name  
from goal, game, goal_reached, airport  
where game_id = game.id  
and goal_id = goal.id  
and screen_name = "Ilkka"  
and game.location = airport.ident;

![Ảnh chụp màn hình 2024-09-13 232439](https://github.com/user-attachments/assets/098a4dee-6edd-4c4e-bd35-3557d9ddf34d)

### 10  
select country.name  
from goal, game, goal_reached, airport, country  
where game_id = game.id  
and goal_id = goal.id  
and screen_name = "Ilkka"  
and game.location = airport.ident  
and airport.iso_country = country.iso_country;

![Ảnh chụp màn hình 2024-09-13 232451](https://github.com/user-attachments/assets/ed278cd8-38f4-4e7f-8ed5-bc6231be0674)
