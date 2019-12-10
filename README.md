# README
## users　table
|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|password|text|null: false, foreign_key: true|
|name|string|null:false, foreign_key: true|
|mail address|text|null: false, foreign_key: true|
|password|string|null: false|
|name|string|null:false|
|mail address|text|null: false|

### Association
- has_many :comments
- has_many :groups, through: :groups_users

## comment　table
|Column|Type|Options|
|------|----|-------|
|image|string|null: false|
|text|text|null: false|

### Association
- belongs_to :user
- belongs_to :group

## group table
|Column|Type|Options|
|------|----|-------|

|name|string|null: false|

### Association
- has_many :users , through: :groups_users
  has_many :comments

## groups_users　table
|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
  belongs_to:group
  belongs_to:user