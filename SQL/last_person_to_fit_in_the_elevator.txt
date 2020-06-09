# Write your MySQL query statement below
SELECT person_name FROM Queue as a
WHERE
(
    SELECT SUM(weight) FROM Queue as b
    WHERE b.turn<=a.turn
    ORDER By turn
)<=1000
ORDER BY a.turn DESC limit 1;