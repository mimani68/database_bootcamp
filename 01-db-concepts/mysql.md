# Mysql [🔗](https://dev.mysql.com/doc/refman/5.7/en)

## Engines

| Title | Description | 
|:-----:|:-----------:|
| InnoDB | InnoDB is a general-purpose storage engine that balances high reliability and high performance.  |
| MyISAM | MyISAM is a high-speed storage and retrieval engine that is suitable for read-heavy applications. InnoDB is a transaction-safe engine that provides standard ACID-compliant transaction features, along with foreign key support |
| MEMORY | The MEMORY storage engine (formerly known as HEAP) creates special-purpose tables with contents that are stored in memory. Because the data is vulnerable to crashes, hardware issues, or power outages, only use these tables as temporary work areas or read-only caches for data pulled from other tables. |
| MERGE | |
| CSV | |

## Indexes

## Cache

## Trigger [🔗](https://dev.mysql.com/doc/refman/5.7/en/trigger-syntax.html)

```mysql
mysql> CREATE TABLE account (acct_num INT, amount DECIMAL(10,2));
Query OK, 0 rows affected (0.03 sec)

mysql> CREATE TRIGGER ins_sum BEFORE INSERT ON account
       FOR EACH ROW SET @sum = @sum + NEW.amount;
Query OK, 0 rows affected (0.01 sec)
mysql> SET @sum = 0;
mysql> INSERT INTO account VALUES(137,14.98),(141,1937.50),(97,-100.00);
mysql> SELECT @sum AS 'Total amount inserted';
+-----------------------+
| Total amount inserted |
+-----------------------+
|               1852.48 |
+-----------------------+
```
