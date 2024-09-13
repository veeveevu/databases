**1**  
select * from goal;
![Ảnh chụp màn hình 2024-09-13 230158](https://github.com/user-attachments/assets/40273543-f88f-4720-8f26-786094c20f2b)

**2**  
select name, type from airport where iso_country like "FI";  
![Ảnh chụp màn hình 2024-09-13 230235](https://github.com/user-attachments/assets/acb769ec-569f-4e6b-b56f-a035a9d8d5a3)

**3**  
select name from airport where iso_country like "FI" order by name asc;
![Ảnh chụp màn hình 2024-09-13 230257](https://github.com/user-attachments/assets/93295e10-5db7-49b9-88f8-18393ee17657)

**4**  
select name, type from airport where iso_country like "FI" order by type asc, name asc;
![Ảnh chụp màn hình 2024-09-13 230316](https://github.com/user-attachments/assets/ee513e49-a010-4be9-963a-789a7a3545b0)

**5**  
select name from country where name like "F%";
![Ảnh chụp màn hình 2024-09-13 230332](https://github.com/user-attachments/assets/b76373b4-cf99-48ea-86c9-db08a57b0876)

**6**  
select name from country where name like "%F%";
![Ảnh chụp màn hình 2024-09-13 230346](https://github.com/user-attachments/assets/cf2a8d4a-f40a-4a8a-821c-d7d0366dcb30)

**7**  
select location from game where screen_name like "Vesa";
![Ảnh chụp màn hình 2024-09-13 230401](https://github.com/user-attachments/assets/b43ee581-7939-4729-bff7-21f6c08b445f)

**8**  
select co2_consumed from game where screen_name like "Ilkka";
![Ảnh chụp màn hình 2024-09-13 230416](https://github.com/user-attachments/assets/a3b32131-ddba-404e-9829-278c12405f7e)

**9**  
select distinct co2_budget from game;
![Ảnh chụp màn hình 2024-09-13 230428](https://github.com/user-attachments/assets/5132028f-ef51-411a-bb14-01b4f79d219e)

**10**  
alter table game add column co2_left int;  
update game set co2_left = co2_budget - co2_consumed;  
select screen_name, co2_budget, co2_consumed, co2_left  
from game where screen_name like "Ilkka";  
![Ảnh chụp màn hình 2024-09-13 230458](https://github.com/user-attachments/assets/56c974c4-3e8f-44f1-95c1-5c26d7a583b5)
