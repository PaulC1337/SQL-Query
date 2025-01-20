# SQL price gap analysis for 06/10/19
Calculating the difference between the maximum and minimum prices for each of the products in the 'milk' category on June 10, 2019. where I am naming the variable max_min_diff.  While converting date values from strings to the date type. while print the product name and the difference between the maximum and minimum price. 

SELECT 
	
 name,
   
    MAX(price)-MIN(price) AS min_max_diff

FROM
 
    products_data_all

WHERE
	
 category='milk'
   
    AND date_upd :: date = '2019-06-10'

GROUP BY
    
    name;
