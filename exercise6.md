# Week 5
## Exercises 6: Aggregate Queries
### 1  
select max(elevation_ft)  
from airport;

![Ảnh chụp màn hình 2024-09-29 162330](https://github.com/user-attachments/assets/058766d5-de63-4efc-a48b-78e29f06ade4)

### 2   
select continent, count(*)  
from country  
group by continent;

![Ảnh chụp màn hình 2024-09-29 162415](https://github.com/user-attachments/assets/0a0526cd-f1ed-4e56-930e-4f9acf4bc996)


### 3  
select screen_name, count(*)  
from game  
join goal_reached on game.id = goal_reached.game_id  
join goal on goal_reached.goal_id = goal.id  
group by screen_name;

![Ảnh chụp màn hình 2024-09-29 162726](https://github.com/user-attachments/assets/3b66cd5b-33f7-49ce-b40b-2f2bbf25d53d)

### 4 
select screen_name  
from game  
group by screen_name  
having min(co2_consumed) = (  
    select min(co2_consumed)  
    from game  
);

![Ảnh chụp màn hình 2024-09-29 162805](https://github.com/user-attachments/assets/721ac299-d8c3-483e-9361-7fc4472efe63)

### 5  

select country.name, count(*)  
from country   
join airport on country.iso_country = airport.iso_country  
group by country.name  
order by count(*) desc, country.name asc  
limit 50;

![Ảnh chụp màn hình 2024-09-29 162847](https://github.com/user-attachments/assets/37781dc7-7b60-4a6a-962f-6147e5884cf3)

### 6  

select country.name  
from country  
join airport on airport.iso_country = country.iso_country  
group by country.name  
having count(airport.id) > 1000;  

![Ảnh chụp màn hình 2024-09-29 162955](https://github.com/user-attachments/assets/d84c6f03-eaca-44dc-af5f-4d6b99cb7b6e)

### 7  

select name  
from airport  
where elevation_ft = (  
select max(elevation_ft)  
from airport  
);

![Ảnh chụp màn hình 2024-09-29 163027](https://github.com/user-attachments/assets/8a391da0-efe5-4250-b4cf-2eea9b7f3eab)

### 8  

select country.name  
from country  
join airport on airport.iso_country = country.iso_country  
where airport.elevation_ft = (  
select max(elevation_ft)  
from airport  
);

![Ảnh chụp màn hình 2024-09-29 163055](https://github.com/user-attachments/assets/839cb0ab-faec-4f21-9923-61279766290a)


### 9 

select count(*)  
from game, goal_reached  
where id = game_id and screen_name = "Vesa"  
group by screen_name;  

![Ảnh chụp màn hình 2024-09-29 163127](https://github.com/user-attachments/assets/49967887-e884-4410-8f32-70644940aceb)

### 10  

select name  
from airport  
order by abs(latitude_deg) desc  
limit 1;

![Ảnh chụp màn hình 2024-09-29 163203](https://github.com/user-attachments/assets/d3a029de-0b97-4918-8345-9f6cee162edb)
