# migration-from-euc-postgresql

EUC-JPで作成されているDBをUTF8に移行する


## Client Encoding

### client_encoding を確認する

```psql
show client_encoding;
```

### client_encoding を変更する

```psql
set client_encoding to SJIS;   -- SJISへ変更
set client_encoding to UTF8;   -- UTF8
set client_encoding to EUC_JP; -- EUC_JPへ変更 
```

## refs

- [PostgreSQLをEUC-JPからUTF-8環境に移行する！](https://qiita.com/saba1024/items/f1da6e4aa0837259cff4)
- [PostgreSQLをEUC-JPからUTF-8環境に移行する！](http://kanndume.blogspot.com/2009/10/postgresqleuc-jputf-8.html)
- [PostgreSQLの文字コードをEUCからUTF-8に変換して移行する](https://plugins.co.jp/2015/03/postgresql%E3%81%AE%E6%96%87%E5%AD%97%E3%82%B3%E3%83%BC%E3%83%89%E3%82%92euc%E3%81%8B%E3%82%89utf-8%E3%81%AB%E5%A4%89%E6%8F%9B%E3%81%97%E3%81%A6%E7%A7%BB%E8%A1%8C%E3%81%99%E3%82%8B/)
- [【psql】文字コード、SQLファイルを指定して結果をファイル出力する](http://www.madeinclinic.jp/%E3%83%87%E3%83%BC%E3%82%BF%E3%83%99%E3%83%BC%E3%82%B9/20191006b/)
- [postgreSQLをEUCからUTF-8に変更してデータ移行する](https://trueman-developer.blogspot.com/2019/10/postgresqleucutf-8.html)
- [EUC-JPなJava Webアプリの文字化けまとめ](https://ooharak.hatenadiary.org/entry/20090809/1249830839)
- [Windows環境でpsqlコマンドを使ってSQLをファイル実行するときにエンコーディングでハマった](https://qiita.com/dkurata38/items/142dbbfd416b86577e5c)
- [PostgreSQLの搭載機能 自動エンコーディング変換の使い方](https://www.unisys.co.jp/solution/tec/atlasbase/s33drt000005ei89-att/dbm_1001_postresql.pdf)
- [RDS for PostgreSQL で SJISのCSVファイルをインサートする](https://dev.classmethod.jp/articles/rds-for-postgresql-sjis-csv-insert/)
- [PostgreSQL の EUC→UTF 変換でエラー発生](https://blog.netandfield.com/shar/2015/04/postgresql-eucutf.html)
- [postgreSQL の文字変換マップをカスタマイズ](http://grep.blog49.fc2.com/blog-entry-87.html)
- [【PostgreSQL】Windowsで文字コード（client_encoding）を変更する](https://postgresweb.com/post-5740)