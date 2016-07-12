# 台日大辭典台語譯本
台日大辭典是1931,1932小川尚義編的。內底的閣有2005林俊育長老拍的字。

中央研究院語言學研究所「閩客語典藏」計畫，有提供[線頂辭典](http://minhakka.ling.sinica.edu.tw/taijittian/)！！

## 原始資料庫資料
原始資料，由`pgsql`dump出來的

## csv資料
由`原始資料庫資料`處理而來，處理環境是Linux Mint 17

1. `TJTST.sql.bz2`解壓縮，得到`TJTST.sql`
2. 安裝`pgsql`，`sudo apt-get install -y postgresql-9.3`
3. 匯入sql到`pgsql`，`cat TJTST.sql | psql`
4. 匯出做csv，進去`psql`，閣來輸入 `\copy (Select * From dic order by id) To '/path/TJTST.csv' With CSV DELIMITER ',' HEADER;`
5. 就可以得到`/path/TJTST.csv'`
