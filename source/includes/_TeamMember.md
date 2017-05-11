# Team Member

## Get Team Member

> Success Response Example

```json
	{
		"user_id": "vasia_pupkin",
		"email": "vasia@pupkin.com",
		"last_name": "Pupkin",
		"first_name": "Vasia",
		"avatar": "http://path/to/avatar.jpg",
		"gravatar": "0bc83cb571cd1c50ba6f3e8a78ef1346",
		"presence": "ACTIVE",
		"created_at": "2017-04-03T12:02:26.548Z",
 		"revision": "763h387348g638g76"
	}
```

### URL

		`TEAM.MEMBER#GET`

### URL Params

Parameter | Type | Required
--------- | ------- | ----------
team_id | String | yes
user_id | String | yes


## Team Members List

> Success Response Example

```json
    {
        "users":
        [
          {
            "user_id": "vasia_pupkin",
            "email": "vasia@pupkin.com",
            "last_name": "Pupkin",
            "first_name": "Vasia",
            "avatar": "http://path/to/avatar.jpg",
            "gravatar": "0bc83cb571cd1c50ba6f3e8a78ef1346",
            "presence": "ACTIVE",
            "created_at": "2017-04-03T12:02:26.548Z",
            "revision": "763h387348g638g76",
          },
        ],
        "revision": "763h387348g638g76"
    }
```

### URL

    `TEAM.MEMBER#LIST`

### URL Params

| Parameter |  Type   |  Required |
|-----------|---------|-----------|
| team_id   |  String |  yes      |


## Create Invitation

> Success Response Example

```json
    {
      "link": "https://strongbox.com/invite/vasiateam/PWOw89vMalPspwBcctRH",
      "token": "PWOw89vMalPspwBcctRH"
    }
```

### URL

    `TEAM.MEMBER.INVITATION#CREATE`

### URL Params

| Parameter   |  Type     |  Required |
|-------------|-----------|-----------|
| team_id     |  String   |  yes      |
| role        |  RoleItem |  yes      |
| open_at     |  Date     |  yes      |
| email       |  String   |           |
| usage_limit |  Int      |           |
| close_at    |  Date     |           |


## Accept Invitation

> Empty Response

### URL

    `TEAM.MEMBER.INVITATION#ACCEPT`

### URL Params

| Parameter |  Type   |  Required |
|-----------|---------|-----------|
| team_id   |  String |  yes      |
| token     |  String |  yes      |


## Leave Team

> Empty Response

### URL

    `TEAM.MEMBER#LEAVE`

### URL Params

| Parameter |  Type   |  Required |
|-----------|---------|-----------|
| team_id   |  String |  yes      |
