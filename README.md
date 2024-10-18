# Bangalore-Traffic-Project

Create database Bangalore_traffic;
use Bangalore_traffic;

select * from b_dataset;

-- Display the average traffic volume for Whitefield 
select round(avg(Traffic_Volume)) as Average_traffic
from b_dataset
where Area_Name="Whitefield";

-- What is the sum of total environmental impact for Mg road
select round(sum(Environmental_Impact)) as Total_Environment
from b_dataset
where Area_Name="M.G. Road";


-- Show the road intersection whose name starts from S
select road
from b_dataset
where road like "S%";

-- Show the character length for all the area name 
select char_length(Area_name),Area_name
from b_dataset;

-- Display the Area name and Road together 
select concat(Area_name,Road) as Total,Area_Name,Road
from b_dataset;

-- Count ther total number of public_transport
select sum(public_transport) as total_public
from b_dataset;
