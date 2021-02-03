# アプリケーション名

# アプリケーション概要

# データベース設計

## users table

|Column             |Type   |Options                   |
|-------------------|-------|--------------------------|
|name           |string |null: false               |
|email              |string |null: false, unique: true |
|encrypted_password |string |null: false               |

### Association

* has_many :items

## item table

|Column              |Type    |Options                        |
|--------------------|--------|-------------------------------|
|user_id             |integer |null: false, foreign_key: true |
|name                |string  |null: false                    |
|price               |integer |null: false                    |
|category_id         |integer |null: false                    |
|status_id           |integer |null: false                    |

### Association

* belongs_to :user