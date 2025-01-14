# Input format of body for train API
## 1. Headers
```python
{
    "Content-Type": "application/json"
}
```
## 2. Body
```python
body_in_train_request = {
    "name_of_model": "test_regression_model",
    "db_credentials": "db_credentials (read below for db_credentials)",
    "training_set_schema": "<optional: if schema present enter schema>",
    "training_set_tableName": "<enter table_name>",
    "input_columns_names": "<enter '*' for all otherwise enter 'col1,col2,col3,..'>",
    "output_column_names": "<enter '*' for all otherwise enter 'col1,col2,col3,..'>"
}
```
## db_credentials format
1. For training the model on your local device
```python
db_credentials = {
    "db_name": "<enter mindsdb database name>",
    "subscription": "local",
    "url":"<optional: if you set custom mindsdb editor port istead of using default>"
}
```
2. For training the model on cloud
```python
db_credentials = {
    "db_name": "<enter mindsdb database name>",
    "subscription": "<optional: default value is 'cloud'>",
    "url":"<optional if using default cloud mindsdb, otherwise required>",
    "email_id": "<email_id>",
    "password": "<password>"
}
```
3. For training the model mindsdb pro
```python
db_credentials = {
    "db_name": "<enter mindsdb database name>",
    "subscription": "pro",
    "url":"<url for pro>",
    "email_id": "<email_id>",
    "password": "<password>"
}
```

