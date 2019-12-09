# README
## users　table

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|password|text|null: false, foreign_key: true|
|name|string|null:false, foreign_key: true|
|mail address|text|null: false, foreign_key: true|

### Association
- has_many :comments
- has_many :groups
- has_many :groups_users


## comment　table

|Column|Type|Options|
|------|----|-------|
|image|string|null: false, foreign_key: true|
|text|string|null: false, foreign_key: true|

### Association
- belongs_to :user
- belongs_to :group


## group table
|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

# Association
- has_many :groups_users
- has_many :users
  has_many :comments



## groups_users　table
|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- has_many:group_id
- has_many:user_id


