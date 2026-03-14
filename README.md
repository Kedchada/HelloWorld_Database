## UserType

| Type | description |
|---|---|
| customer | customer of the system |
| admin | manager of the system |

## User

| Attribute | Data Type | Description | Constraints |
|---|---|---|----|
| user_id | serial | unique identifier of user | Primary Key |
| firstname | varchar(255) | user's firstname | Not Null |
| surname | varchar(255) | user's surname | Not Null |
| phonenumber | varchar(10) | user's phonenumber | Not Null |
| user_type | UserType | role of the user | default: customer | 

## Appointment

| Attribute | Data Type | Description | Constraints |
|---|---|---|----|
| appointment_id | serial | unique identifier of appointment | Primary Key |
| broken_part | varchar(255) | the part of the car that is broken and need to fixed | None |
| short_description | varchar(255) | brief description of the appointment| |
| user_id | integer | user id of the user that created this appointment | Foreign Key, Not Null |
| car_id | integer | car id of the car that needs fixing | Foreign Key, Not Null |

## Car

| Attribute | Data Type | Description | Constraints |
|---|---|---|----|
| car_id | serial | unique of car | Primary Key |
| brand | varchar(255) | brand of the car | Not Null |
| model | varchar(255) | model of the car | Not Null |
| owner | integer | owner of the car | Not Null |

## Movie

| Attribute | Data Type | Description | Constraints |
|---|---|---|----|
| movie_id | serial | unique of movie | Primary Key |
| category_id | integer | category of the movie | Not Null |
| title | varchar(255) | name of the title | Not Null |
| duration | varchar(255) | time of the movie | Not Null |
| dub_language | varchar(255) | language of the movie | Not Null |
| sub_language | varchar(255) | language sub of the movie | NOt Null |

## Customer
| Attribute | Data Type | Description | Constraints |
|---|---|---|----|
| customer_id | serial | unique of customer | Primary Key |
| firstname | varchar(255) | customer firstname | Not Null |
| surname | varchar(255) | customer surname | Not Null |
