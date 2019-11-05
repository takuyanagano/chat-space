# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...

userテーブル

|Column|Type|Options|
|------|----|-------|
|e-mail|string|null: false|
|user_name|string|null: false|

Association
- has_many :groups_users
- has_many :groups, through: :groups_users
- has_many :message


groupテーブル

|Column|Type|Option|
|------|----|------|
|group_name|string|null: false|
|user_id|integer|null: false, foreign_key: ture|

Association
- has_many :groups_users
- has_many :users, throgh: :groups_users
- has_many :message


groups_usersテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: ture|
|group_id|integer|null: false, foreign_key: ture|

Association
- belongs_to :user
- belongs_to :group


messageテーブル

|Column|Type|Options|
|------|----|-------|
|body|text||
|image|string||
|user_id|integer|null: false, foreign_key: ture|
|group_id|integer|null: false, foreign_key: ture|

Association
- belongs_to :user
- belongs_to :group

# README
## how to use GitHub Desktop
## how to use git revert