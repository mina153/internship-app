# README

#テーブル設計

##users（ユーザー情報）テーブル

| Column              | Type    | Options                      |
|---------------------|---------|------------------------------|
| name                | string  | null:false                   |
| email               | string  | null:false, uniqueness: true |
| encrypted_password  | string  | null:false                   |
| birth_date          | date    | null:false                   |

### Association

- has_many :companies

##companies (会社情報)テーブル

| Column                 | Type       | Options                      |
|------------------------|------------|----------------------------- |
| company_name           | string     | null:false                   |
| explanation            | text       | null:false                   |
| my_id                  | string     | null:false                   |
| my_password            | string     | null:false                   |
| date                   | date       | null:false                   |
| user                   | references | null:false,foreign_key: true |

### Association

- belongs_to :user

