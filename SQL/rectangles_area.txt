# Write your MySQL query statement below
SELECT a.id as p1,b.id as p2,abs(a.x_value-b.x_value)*abs(a.y_value-b.y_value) as area
FROM Points as a
JOIN Points as b
ON a.x_value!=b.x_value AND a.y_value!=b.y_value AND a.id<b.id
ORDER BY area DESC, p1 ASC, p2 ASC;