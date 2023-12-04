# 數據定義
## 建（CREATE）
### 數據庫（DATABASE）
```
建庫「庫名」。
```
- 文字唯[十六式](en.wikipedia.org/UTF-16)是用。
### 事務（EVENT）
```
建事「事名」[若無][於<時刻>|每<時間>自<時刻>至<時刻>]。
      <語句>
事畢。
```
### 函數（FUNCTION/PROCEDURE）
```
建術「術名」（{入|出|出入}「形參」，...）。
      <語句>
術畢。
```
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
建表[若無]「表名」（「列名」<列義>，...[，限（式）]）。
建表[若無]「表名」如「表名」。
建表[若無]「表名」<取語句>。
列義：〈品類〉[置（式）][隱][獨]
      [依「表名」[去{從|逆|復}][改{從|逆|復}]]。
```
- [彼](https://dev.mysql.com/doc/refman/8.0/en/create-table.html)以限（CONSTRAINT）字明主（PRIMARY）、獨（UNIQUE）、外鍵（FOREIGN KEY），徒增文長，吾不用也。
- `〈品類〉`視[此](../guide.md)。
- 從：所依去則去之，所依改則改之。
- 逆：所依或不得去，或不得改。
- 復：所依或去或改則復於零。
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
改表「表名」<方法>。
方法: 
  |增 （「列名」<列義>，...）[先「列名」|末]
  |列「列名」〈品類〉[置（式）][隱|顯][獨|去獨]
      [依「表名」[去{從|逆|復}][改{從|逆|復}]|去依]。
  |列「列名」名「新列名」
  |去列「列名」
  |限（式）
  |去限
  |名「新表名」。
列義：〈品類〉[置（式）][隱][獨]
      [依「表名」[去{從|逆|復}][改{從|逆|復}]]。
```

### 表組（TABLESPACE）
### 觸發器（TRIGGER）
### 視圖（VIEW）
## 清表
```
清[表]「表名」
```
