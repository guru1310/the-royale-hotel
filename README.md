# the-royale-hotel

1. Open MySQL 8.0 Command line CLient

2. If using cmd,
   type: mysql -u root -p

3. create database;

4. create tables:
+----------------------------+
| Tables_in_hotel_management |
+----------------------------+
| amenities                  |
| bookings                   |
| customers                  |
| payments                   |
| records                    |
| reviews                    |
| rooms                      |
| rooms_section              |
+----------------------------+
+--------------+------------+------+-----+---------+----------------+
| Field        | Type       | Null | Key | Default | Extra          |
+--------------+------------+------+-----+---------+----------------+
| AMENITY_ID   | int        | NO   | PRI | NULL    | auto_increment |
| ROOM_ID      | int        | YES  | MUL | NULL    |                |
| AMENITY_NAME | char(50)   | YES  |     | NULL    |                |
| IS_AVAILABLE | tinyint(1) | NO   |     | NULL    |                |
+--------------+------------+------+-----+---------+----------------+
+------------------+---------------+------+-----+---------+----------------+
| Field            | Type          | Null | Key | Default | Extra          |
+------------------+---------------+------+-----+---------+----------------+
| BOOKING_ID       | int           | NO   | PRI | NULL    | auto_increment |
| CUSTOMER_ID      | int           | YES  | MUL | NULL    |                |
| ROOM_ID          | int           | YES  | MUL | NULL    |                |
| CHECK_IN_DATE    | date          | NO   |     | NULL    |                |
| CHECK_OUT_DATE   | date          | NO   |     | NULL    |                |
| NUMBER_OF_NIGHTS | int           | NO   |     | NULL    |                |
| TOTAL_PRICE      | decimal(10,2) | NO   |     | NULL    |                |
| PAYMENT_METHOD   | char(20)      | YES  |     | NULL    |                |
| STATUS           | char(10)      | NO   |     | NULL    |                |
+------------------+---------------+------+-----+---------+----------------+
+--------------+-----------+------+-----+-------------------+-------------------+
| Field        | Type      | Null | Key | Default           | Extra             |
+--------------+-----------+------+-----+-------------------+-------------------+
| CUSTOMER_ID  | int       | NO   | PRI | NULL              | auto_increment    |
| NAME         | char(50)  | NO   |     | NULL              |                   |
| PHONE_NUMBER | char(10)  | NO   |     | NULL              |                   |
| EMAIL_ID     | char(50)  | NO   |     | NULL              |                   |
| ADDRESS      | text      | YES  |     | NULL              |                   |
| CREATED_AT   | timestamp | YES  |     | CURRENT_TIMESTAMP | DEFAULT_GENERATED |
+--------------+-----------+------+-----+-------------------+-------------------+
+----------------+---------------+------+-----+---------+----------------+
| Field          | Type          | Null | Key | Default | Extra          |
+----------------+---------------+------+-----+---------+----------------+
| PAYMENT_ID     | int           | NO   | PRI | NULL    | auto_increment |
| BOOKING_ID     | int           | YES  | MUL | NULL    |                |
| PAYMENT_DATE   | date          | NO   |     | NULL    |                |
| PAYMENT_AMOUNT | decimal(10,2) | NO   |     | NULL    |                |
| PAYMENT_METHOD | char(20)      | YES  |     | NULL    |                |
| PAYMENT_STATUS | char(20)      | YES  |     | NULL    |                |
+----------------+---------------+------+-----+---------+----------------+
+--------------+----------+------+-----+---------+-------+
| Field        | Type     | Null | Key | Default | Extra |
+--------------+----------+------+-----+---------+-------+
| NAME         | char(50) | YES  |     | NULL    |       |
| PHONE_NUMBER | char(10) | YES  |     | NULL    |       |
| EMAIL_ID     | char(50) | YES  |     | NULL    |       |
| PASSWORD     | char(50) | YES  |     | NULL    |       |
+--------------+----------+------+-----+---------+-------+
+-------------+-----------+------+-----+-------------------+-------------------+
| Field       | Type      | Null | Key | Default           | Extra             |
+-------------+-----------+------+-----+-------------------+-------------------+
| REVIEW_ID   | int       | NO   | PRI | NULL              | auto_increment    |
| ROOM_ID     | int       | YES  | MUL | NULL              |                   |
| CUSTOMER_ID | int       | YES  | MUL | NULL              |                   |
| REVIEW_TEXT | text      | YES  |     | NULL              |                   |
| RATING      | int       | NO   |     | NULL              |                   |
| CREATED_AT  | timestamp | YES  |     | CURRENT_TIMESTAMP | DEFAULT_GENERATED |
+-------------+-----------+------+-----+-------------------+-------------------+
+-------------+---------------+------+-----+---------+----------------+
| Field       | Type          | Null | Key | Default | Extra          |
+-------------+---------------+------+-----+---------+----------------+
| ROOM_ID     | int           | NO   | PRI | NULL    | auto_increment |
| ROOM_NUMBER | char(10)      | NO   |     | NULL    |                |
| ROOM_TYPE   | char(30)      | NO   |     | NULL    |                |
| PRICE       | decimal(10,2) | NO   |     | NULL    |                |
| STATUS      | char(10)      | NO   |     | NULL    |                |
| DESCRIPTION | text          | YES  |     | NULL    |                |
+-------------+---------------+------+-----+---------+----------------+
+-----------+---------------+------+-----+---------+----------------+
| Field     | Type          | Null | Key | Default | Extra          |
+-----------+---------------+------+-----+---------+----------------+
| BK_ID     | int           | NO   | PRI | NULL    | auto_increment |
| BK_DATE   | date          | YES  |     | NULL    |                |
| BK_TIME   | time          | YES  |     | NULL    |                |
| NAME      | char(50)      | YES  |     | NULL    |                |
| PH_NO     | char(10)      | YES  |     | NULL    |                |
| EMAIL_ID  | char(50)      | YES  |     | NULL    |                |
| RM_TYPE   | char(30)      | YES  |     | NULL    |                |
| RATE_PD   | decimal(10,2) | YES  |     | NULL    |                |
| NO_RM     | int           | YES  |     | NULL    |                |
| CHKIN_DT  | date          | YES  |     | NULL    |                |
| CHKOUT_DT | date          | YES  |     | NULL    |                |
| NO_DAYS   | int           | YES  |     | NULL    |                |
| TOTAL_AMT | decimal(10,2) | YES  |     | NULL    |                |
| PAY_MTD   | char(20)      | YES  |     | NULL    |                |
+-----------+---------------+------+-----+---------+----------------+

5. Run the python code and Enjoy!
