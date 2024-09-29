# Week 5
## Exercises 7: Update Queries

### 1  

update game
set location = (
    select ident
    from airport
    where name = 'Nottingham Airport'
),
co2_consumed = co2_consumed + 500
where screen_name = 'Vesa';

Note: I did not include the screenshot because I do not want to modify the original database.

### 2   

Prepare your own database for the project by deleting all dummy data relating to the game state. To maintain referential integrity, you have to delete the data in a specific order.

Do you have to delete data first from the game table or from the goal_reached table?

a.goal_reached

### 3  

delete from goal_reached;

### 4  

delete from game;
