# テーブル設計

## users テーブル

| Column             | Type   | Options     |
| ------------------ | ------ | ----------- |
| name               | string | NOT NULL    |
| email              | string | NOT NULL    |
| encrypted_password | string | NOT NULL    |
| profile            | text   | NOT NULL    |
| occupation         | text   | NOT NULL    |
| position           | text   | NOT NULL    |


## comments テーブル

| Column    | Type       | Options                      |
| --------- | ---------- | ---------------------------- |
| content   | text       | NOT NULL                     |
| prototype | references | NOT NULL , foreign_key: true | 
| user      | references | NOT NULL , foreign_key: true |


## room_users テーブル

| Column     | Type       | Options                        |
| ---------- | ---------- | ------------------------------ |
| user       | references | NOT NULL , foreign_key: true   |
| title      | string     | NOT NULL                       |
| catch_copy | text       | NOT NULL                       |
| concept    | text       | NOT NULL                       |
