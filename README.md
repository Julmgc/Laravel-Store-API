​<div align ="center">

## <font size="7">**Store API**</font>

</div>
<br></br>
<div align ="center" >

<font size="6">Description </font>

</div>
<br></br>
<div align ="center" font size="4">
<font size="4">This is an API for a store and products, the technologies used were, PHP, Laravel and SQLite.

License: MIT</font>

<div align ="center" font size="4">
<font size="4">On your terminal:

make a copy of this project

git@github.com:Julmgc/Laravel-Store-API.git

cd Laravel-Store-API

To create the tables run:

php artisan migrate

To populate the db:

php artisan db:seed

To run your server type:

php artisan serve

In order to use this app you should use an application for HTTP client, like postman, insomnia, etc.</font>

</div>
</div>
<div align ="center" >

<font size="6">Base URL: </font>

</div>
<div align ="center">
<font size="4">/api</font>
</div>

​<div align ="center">

<font size="4">POST /store/</font>
<br></br>
<font size="4">Create a store</font>

</div>

<br></br>
<font color="caramel"> Request </font>
​

```json
{
    "name": "Furniture store"
}
```

​
<font color="yellow"> _Response_ </font>
​

```json
{
    "name": "Furniture Store",
    "description": "A great store",
    "updated_at": "2022-05-23T17:32:02.000000Z",
    "created_at": "2022-05-23T17:32:02.000000Z",
    "id": 13
}
```

​​<div align ="center">

<font size="4">GET /stores/</font>
<br></br>
<font size="4">List of all stores</font>

</div>

<font color="caramel"> Response </font>

```json
{
    "current_page": 1,
    "data": [
        {
            "id": 1,
            "name": "Furniture Store",
            "description": "great store",
            "created_at": "2022-05-23T15:49:33.000000Z",
            "updated_at": "2022-05-23T17:05:04.000000Z"
        },
        {
            "id": 2,
            "name": "perspiciatis dolorum eius",
            "description": "Tenetur voluptate dolor est voluptates unde et cumque ad.",
            "created_at": "2022-05-23T17:18:51.000000Z",
            "updated_at": "2022-05-23T17:18:51.000000Z"
        },
}
```

<br></br>

<div align ="center">

<font size="4">PUT /stores/<int:store_id>/</font>
<br></br>
<font size="4">Change a store name and description</font>
<br></br>

</div>

<font color="caramel"> Request </font>

```json
{
    "name": "Confy",
    "description": "Chairs store"
}
```

​
<font color="yellow"> _Response_ </font>
​

```json
{
    "id": 1,
    "name": "Confy",
    "description": "Chairs store",
    "created_at": "2022-05-23T15:49:33.000000Z",
    "updated_at": "2022-05-23T17:34:03.000000Z"
}
```

<br></br>

<div align ="center">

<font size="4">PATCH /stores/<int:store_id>/</font>
<br></br>
<font size="4">Change a store name or description</font>
<br></br>

</div>

<font color="caramel"> Request </font>

```json
{
    "description": "Red chairs store"
}
```

​
<font color="yellow"> _Response_ </font>
​

```json
{
    "id": 1,
    "name": "Confy",
    "description": "Red chairs store",
    "created_at": "2022-05-23T15:49:33.000000Z",
    "updated_at": "2022-05-23T17:34:03.000000Z"
}
```

<br></br>

<div align ="center">

<font size="4">Delete a store</font>
<font size="4">DELETE /stores/<int:course_id>/</font>
<br></br>

</div>

​
