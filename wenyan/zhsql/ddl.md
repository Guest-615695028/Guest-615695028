# 數據定義
## 建（CREATE）
### 數據庫（DATABASE）
```
建庫「庫名」。
```
### 事務（EVENT）
### 函數（FUNCTION/PROCEDURE）
### 索引（INDEX）
廢。表以行索。
### 記錄（LOGFILE GROUP）
廢。
### 服務器（SERVER）
廢。
### 空間參考系（SPATIAL REFERENCE SYSTEM）
廢。
### 表（TABLE）
表必有首，首以行（音航）序，自一而增，斷處先補。故`行`字不可以爲列名。
> 斷：首`甲`有行而`甲加一`無之，則`甲加一`爲斷處；首`一`無行，則`一`是也。
```
建表[若無]「表名」({「列名」<列義>}...[限（式）])
    [<劃分>...]。
建表[若無]「表名」如「表名」
建表[若無]「表名」取（取語句）
列義：〈品類〉[置（式）][隱][獨]
      [依「表名」[去{從|棄}][改{從|棄}]]。
```
- [彼](https://dev.mysql.com/doc/refman/8.0/en/create-table.html)以限（CONSTRAINT）字明主（PRIMARY）、獨（UNIQUE）、外鍵（FOREIGN KEY），徒增文長，吾不用也。
- `〈品類〉`視[此](../guide.md)。
### 表組（TABLESPACE）
### 觸發器（TRIGGER）
### 視圖（VIEW）
## 去（DROP）
### 數據庫（DATABASE）
### 事務（EVENT）
### 函數（FUNCTION/PROCEDURE）
### 索引（INDEX）
### 記錄（LOGFILE GROUP）
### 服務器（SERVER）
### 空間參考系（SPATIAL REFERENCE SYSTEM）
### 表（TABLE）
### 表組（TABLESPACE）
### 觸發器（TRIGGER）
### 視圖（VIEW）
## 改（ALTER）
### 數據庫（DATABASE）
### 事務（EVENT）
### 函數（FUNCTION/PROCEDURE）
### 索引（INDEX）
### 記錄（LOGFILE GROUP）
### 服務器（SERVER）
### 空間參考系（SPATIAL REFERENCE SYSTEM）
### 表（TABLE）
```
改表「表名」
    [<方法> [, <方法>] ...]。

<方法>: 
  |增列「列名」<列義>[先「列名」|末]
  |增列 (「列名」 column_definition,...)
  |增限（式）
  |去限
  | ALTER {CHECK | CONSTRAINT} symbol [NOT] ENFORCED
  | ALGORITHM [=] {DEFAULT | INSTANT | INPLACE | COPY}
  |改列 「列名」 {
        SET DEFAULT {literal | (expr)}
      | SET {VISIBLE | INVISIBLE}
      | DROP DEFAULT
    }
  | ALTER INDEX index_name {VISIBLE | INVISIBLE}
  | CHANGE 列 old_「列名」 new_「列名」 column_definition
        [FIRST | AFTER 「列名」]
  | [DEFAULT] CHARACTER SET [=] charset_name [COLLATE [=] collation_name]
  | CONVERT TO CHARACTER SET charset_name [COLLATE collation_name]
  | {DISABLE | ENABLE} KEYS
  | {DISCARD | IMPORT} TABLESPACE
  | DROP 列 「列名」
  | DROP {INDEX | KEY} index_name
  | DROP PRIMARY KEY
  | DROP FOREIGN KEY fk_symbol
  | FORCE
  | LOCK [=] {DEFAULT | NONE | SHARED | EXCLUSIVE}
  | MODIFY 列 「列名」 column_definition
        [FIRST | AFTER 「列名」]
  | ORDER BY 「列名」 [, 「列名」] ...
  | RENAME COLUMN old_「列名」 TO new_「列名」
  | RENAME {INDEX | KEY} old_index_name TO new_index_name
  | RENAME [TO | AS] new_tbl_name
  | {WITHOUT | WITH} VALIDATION。

key_part: {「列名」 [(length)] | (expr)} [ASC | DESC]
```
### 表組（TABLESPACE）
### 觸發器（TRIGGER）
### 視圖（VIEW）
## 清表
```
清[表]「表名」
```
