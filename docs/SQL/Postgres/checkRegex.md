SELECT * FROM books WHERE title ~ '^[0-9]'

ou 

SELECT * FROM books WHERE CAST(price AS TEXT) LIKE '123%'

https://stackoverflow.com/questions/1684291/sql-like-condition-to-check-for-integer