## usersテーブル

| Column | Type       | Options                        |
| ------ | ---------- | ------------------------------ |
| email   | string | null: false, unique: true |
| encrypted_password  | string | null: false|
| name  | string | null: false|
| profile  | text | null: false|
| occupation  | text | null: false|
| position  | text | null: false|

### Association
- belongs_to :prototypes
- belongs_to :comments

## prototypesテーブル

| Column | Type       | Options                        |
| ------ | ---------- | ------------------------------ |
| user   | references | null: false, foreign_key: true |
| group  | references | null: false, foreign_key: true |

### Association
- belongs_to :group
- belongs_to :user

## commentsテーブル

| Column | Type       | Options                        |
| ------ | ---------- | ------------------------------ |
| user   | references | null: false, foreign_key: true |
| group  | references | null: false, foreign_key: true |

### Association
- belongs_to :group
- belongs_to :user