# Restaurant-Order-Analysis

use restaurant_db;

-- 1. View menu_items table.alter
select * from menu_items;

-- 2. Find the number of items on menu.
select count(*) from menu_items;

-- 3. What are the least and most expensive itesm on the menu.
select * from menu_items  -- least
order by price;

select * from menu_items  -- most
order by price desc;

-- 4. How many Italian dishes are on the menu. 
select count(*) from menu_items
where category = "Italian";

-- 5. What are the least and most expensive Italian dishes on the menu.
select * from menu_items
where category = "Italian"
order by price;

select * from menu_items
where category = "Italian"
order by price desc;

-- 6. How many dishes are in each catrgory.
select category, count(menu_item_id) as num_dishes
from menu_items
group by category;

-- 7. What is the avg dish price within each category.
select category, avg(price) as avg_price
from menu_items
group by category;


