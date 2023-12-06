# Mysql [🔗](https://dev.mysql.com/doc/refman/5.7/en)

## Transaction

```mysql
START TRANSACTION;

-- Your SQL statements here
INSERT INTO table1 (column1) VALUES (value1);
UPDATE table2 SET column2 = value2 WHERE condition;
DELETE FROM table3 WHERE condition;

COMMIT;
```

## Engines

| Title | Description | 
|:-----:|:-----------:|
| InnoDB | InnoDB is a general-purpose storage engine that balances high reliability and high performance.  |
| MyISAM | MyISAM is a high-speed storage and retrieval engine that is suitable for read-heavy applications. InnoDB is a transaction-safe engine that provides standard ACID-compliant transaction features, along with foreign key support |
| MEMORY | The MEMORY storage engine (formerly known as HEAP) creates special-purpose tables with contents that are stored in memory. Because the data is vulnerable to crashes, hardware issues, or power outages, only use these tables as temporary work areas or read-only caches for data pulled from other tables. |
| MERGE | |
| CSV | |

## Indexes

| Title | Description |
|:-----:|:-----------:|
| Primary Key | The primary key for a table represents the column or set of columns that you use in your most vital queries. It has an associated index, for fast query performance. Query performance benefits from the NOT NULL optimization, because it cannot include any NULL values. With the InnoDB storage engine, the table data is physically organized to do ultra-fast lookups and sorts based on the primary key column or columns. |
| SPATIAL | The optimizer checks the SRID attribute for indexed columns to determine which spatial reference system (SRS) to use for comparisons, and uses calculations appropriate to the SRS. |
|  |  |

## Cache

## Optimization [🔗](https://dev.mysql.com/doc/refman/5.7/en/switchable-optimizations.html)

```mysql
mysql> SET optimizer_switch='index_merge_union=off,index_merge_sort_union=off';

mysql> SELECT @@optimizer_switch\G
*************************** 1. row ***************************
@@optimizer_switch: index_merge=on,index_merge_union=off,
                    index_merge_sort_union=off,
                    index_merge_intersection=on,
                    engine_condition_pushdown=on,
                    index_condition_pushdown=on,
                    mrr=on,mrr_cost_based=on,
                    block_nested_loop=on,batched_key_access=off,
                    materialization=on,semijoin=on,loosescan=on,
                    firstmatch=on,duplicateweedout=on,
                    subquery_materialization_cost_based=on,
                    use_index_extensions=on,
                    condition_fanout_filter=on,derived_merge=on,
                    prefer_ordering_index=on
```

## Lock database

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
