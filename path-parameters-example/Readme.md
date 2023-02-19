# Path Parameters Example

## Description 

This example demonstrates use of api gateway path parameters.

It contains 2 event listeners:

GET /service/:a/:b/:c 
This api contains 3 path parameters named: a, b, c

Service returns payload 
```
{
    "service": "a-b-c",
    "a": "value of path parameter a",
    "b": "value of path parameter b",
    "c": "value of path parameter c",
}
```

GET /service/:a/:b/
This api contains 2 path parameters named: a, b

Service returns payload 
```
{
    "service": "a-b",
    "a": "value of path parameter a",
    "b": "value of path parameter b"
}
```

## Test

Each event lister has defined test case

## Deployment and run as lambda

The easiest way to deploy is using kumologica designer. 

1. On AWS tab, select profile and press connect. 
2. Make sure that "Amazon API Gateway" and "Create new API" are selected under triggers section
3. Press Deploy button

The api will be available under urls:

1. GET https://{ api id }.execute-api.{ region }.amazonaws.com/{ stage }/service/:a/:b/:c
2. GET https://{ api id }.execute-api.{ region }.amazonaws.com/{ stage }/service/:a/:b
