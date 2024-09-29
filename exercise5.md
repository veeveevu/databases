# Week 4
## Exercises 5: Subqueries
### 1  
select name  
from country  
where iso_country in (  
    select iso_country  
    from airport  
    where name like 'Satsuma%'  
);

![Ảnh chụp màn hình 2024-09-29 050157](https://github.com/user-attachments/assets/2e033f2d-d8d2-474b-90e2-a2f8a78bd1b9)

### 2   
select name  
from airport  
where iso_country in (  
    select iso_country  
    from country  
    where name like "Monaco"  
);

![Ảnh chụp màn hình 2024-09-29 050508](https://github.com/user-attachments/assets/4b36eab4-eb03-4687-a3f4-1f554ce46813)

### 3  
select game.screen_name  
from game  
where id in (  
    select game_id  
    from goal_reached, goal  
    where goal_reached.goal_id = goal.id  
    and goal.name like "CLOUDS"  
);

![Ảnh chụp màn hình 2024-09-29 051022](https://github.com/user-attachments/assets/46584787-e5b5-4dc5-9d8a-fd619ef4604d)

### 4  
select name  
from country  
where iso_country not in (  
    select iso_country  
    from airport  
);  

![Ảnh chụp màn hình 2024-09-29 051216](https://github.com/user-attachments/assets/88005f6b-49bd-4546-8da1-fd8b66856ff4)

### 5  
from goal  
where id not in (  
    select goal_id  
    from goal_reached, game  
    where screen_name like "Heini"   
);

![Ảnh chụp màn hình 2024-09-29 051656](https://github.com/user-attachments/assets/f7aa9505-13d5-4597-95a5-07cd0ebb0d01)
