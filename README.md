# cricket_api

API to access cricket stats like Players,Venues,Match Details.

# Description

A Cricket API with Flask and API building. 
# Resources

| Resource | Parameters                   |
|---------|------------------------------|
|players|`id`, `age`, `country_code`, `full_name`, `playing_role`, `team_id`|
|teams| `id`, `losses`, `matches_played`, `name`, `wins`|
|countries|`code`, `name`|
|venues| `id`, `country_code`, `name`|
|matches| `id`, `best_fielder`, `bowler_of_the_match`, `loser`, `man_of_the_match`, `winner`|
# Usage
Base URL - `hostname/api/v1/resources/`

## GET


#### *GET `/api/v1/resources/{resource}/all`*

For getting all values of a resource type (default 20)  

> **Example:** GET `/api/v1/resources/players/all`

The above example will return 20 records of type `player`, to change the number of records use the `count` parameter

> **Example:** GET `/api/v1/resources/players/all?count=100`  

---

#### *GET `api/v1/resources/{resource}/{id}`*

 For getting a resource by id 

> **Example:** GET `/api/v1/resources/players/1`

---
#### *GET `api/v1/resources/{resource1}?{param1}={value1}&{param2}={value2}...`*

For getting values of a resource by filtering using parameters

> **Example:** GET `/api/v1/resources/players?playing_role=Batsman  

---
## POST

#### *POST `/api/v1/resources/{resource}?{param1}={value1}&...`*

For creating a new record of a resource type

> **Example:** POST `/api/v1/resources/teams?losses=0&matches_played=0...`

---

## PUT

#### *PUT `api/v1/resources/{resource}/{id}?{param1}={new_value1}&{param2}={new_value2}...`*

For updating a record of a resource
> **Example:** PUT `/api/v1/resources/players/2?team_id=3`

---
## DELETE


#### *DELETE `api/v1/resources/{resource}/{id}`*
Delete record of resource by id 
> **Example:** DELETE `/api/v1/resources/players/2`
