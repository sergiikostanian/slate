# Workspace

## Create Workspace

> Success Response Example

```json
  {
    "workspace_id": "VasiaWorkspace",
    "revision": "y3GSL3ONP38lfFRhZiCA1w"
  }
```

### URL

    `TEAM.WORKSPACE#CREATE`

### URL Params

| Parameter    |  Type   |  Required |
|--------------|---------|-----------|
| team_id      |  String |  yes      |
| workspace_id |  String |  yes      |
| name         |  String |           |
| description  |  String |           |
| private      |  Bool   |           |


## Get Workspace

> Success Response Example

```json
  {
    "workspace_id": "VasiaWorkspace",
    "cover": "http://path/to/cover.jpg",
    "created_at": "2017-04-12T13:42:24.000Z",
    "description": "",
    "name": "",
    "participating": 1,
    "private": false,
    "revision": "349445385978120193",
    "thumbnail": "",
    "unread_message_count": 0,
  }
```

### URL

    `TEAM.WORKSPACE#GET`

### URL Params

| Parameter    |  Type   |  Required |
|--------------|---------|-----------|
| team_id      |  String |  yes      |
| workspace_id |  String |  yes      |


## Workspaces List

> Success Response Example

```json
  {
    "workspaces": [
      {
        "workspace_id": "VasiaWorkspace",
        "cover": "http://path/to/cover.jpg",
        "created_at": "2017-04-12T13:42:24.000Z",
        "description": "",
        "name": "",
        "participating": 1,
        "private": false,
        "revision": "349445385978120193",
        "thumbnail": "",
        "unread_message_count": 0,
      },
    ],
    "revision": "349445385978120193"
  }
```

### URL

    `TEAM.WORKSPACE#LIST`

### URL Params

| Parameter    |  Type   |  Required |
|--------------|---------|-----------|
| team_id      |  String |  yes      |


## Workspace Availability

> Success Response Example

```json
  {
    "available": true
  }
```

### URL

    `TEAM.WORKSPACE#AVAILABILITY.CHECK`

### URL Params

| Parameter    |  Type   |  Required |
|--------------|---------|-----------|
| team_id      |  String |  yes      |
| workspace_id |  String |  yes      |
