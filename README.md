# African-Marketplace-Backend

## Base URL https://web-45-heroku-tb.herokuapp.com/api

## Auth

### POST (Register)
<details>
    <summary>https://web-45-heroku-tb.herokuapp.com/api/auth/register</summary>

    Body Requirements:

    username (string) (required)
    password (string) (required)
    
    You will receive a registered user object.

    Example Result:

    { 
        "username": "jimmy",
        "password": "$2a$08$eVblG7WByjvUTGkXnJVQKOD2E9w34DV1I0MDJ9CTlLfkpCu/UOAju",
    }
</details>

### POST (Login)
<details>
    <summary>https://web-45-heroku-tb.herokuapp.com/api/auth/login</summary>

    Body Requirements:

    username (string) (required)
    password (string) (required)

    You will receive a welcome back message with the user's token.

    Example Result:

    {
        "message": "welcome jimmy",
        "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWJqZWN0IjozLCJ1c2VybmFtZSI6Im5ldmlsbGUiLCJpYXQiOjE2MjczMTgyNzcsImV4cCI6MTYyNzQwNDY3N30.-fR-iAg5RggE9HpWAScdHxlxwknxw7wx0nMxGgQbqpI"
    }
</details>

## Items

### GET
<details>
    <summary>https://web-45-heroku-tb.herokuapp.com/api/items</summary>

    You will receive an array of item objects.

    Example Result:

    [
        {
            item_id: 1,
            item_name: 'Eggs',
            item_category: 'Animal Products',
            item_price: 2,
            item_description: 'Fresh, organic, cage-free eggs',
        },
        {
            item_id: 2,
            item_name: 'Ham',
            item_category: 'Animal Products',
            item_price: 8,
            item_description: 'Fresh, organic, cage-free ham',
        }
    ]

</details>

### POST

<details>
    <summary>https://web-45-heroku-tb.herokuapp.com/api/items</summary>

    Body Requirements:

    item_name (string) (required)
    item_category (string) (required)
    item_price (integer) (required)
    item_description (string) (required)

</details>

### PUT
<details>
    <summary>https://web-45-heroku-tb.herokuapp.com/api/items/:id</summary>

    Item Update Options:

    item_name (string)
    item_category (string)
    item_price (integer)
    item_description (string)

    You will receive a an updated item object.

    Example Result:

    {
        item_id: 2,
        item_name: Eggs,
        item_category: Animal Products,
        item_price: 3000,
        item_description: Fresh, organic, cage-free eggs,
    }

</details>

### DELETE
<details>
    <summary>https://web-45-heroku-tb.herokuapp.com/api/items/:id</summary>

    You will receive an object containing data from the deleted item.

    Example Result:

    {
        item_id: 1,
        item_name: Eggs,
        item_category: Animal Products,
        item_price: 2,
        item_description: Fresh, organic, cage-free eggs,
    }
    
</details>
