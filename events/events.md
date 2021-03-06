# Events

The document content definition servicies from **Events** microservice

## Services

* [Get Event List](#EventList)  `
* [Confirm assisstant ](#ConfirmAssisstant)  


### Get Event List


Use this service to get the events.

#### Request

* URL: /v1.0/student/{student_id}/events
* Method: GET

#### Response

* HTTP Status: 200 (Ok)
* Body:

``` json
{
    "info": {
        "type": "success",
        "sessionId": "gTfI0uOuSZzl4d2nA4no5PIqrktzRgXu..."
    },
    "responseContent": {
        "events": [{
                "id": 1,
                "title": "Dia de las Madres",
                "description": "Invitamos este 10 de Mayo a todas las madres...",
                "icon" : 10,
                "need_assisstance" : false,
                "assisstance" : true,
                "need_payment" : true,
                "paid" : false,
                "formatted_date": "10 de Mayo 10:00 AM"
            },
            {
                "id": 2,
                "title": "Reunion de entrega de notas",
                "description": "La entrega de notas se realizará durante toda la mañana,se suspenden clases de los alumnos.",
                "icon" : 11,
                "need_assisstance" : true,
                "assisstance" : false,
                "need_payment" : false,
                "need_payment" : false,
                "paid" : false,
                "formatted_date": "15 de Mayo 08:00 AM"
            },
        ]
    }
}
```

[Return](#EventList)

### Confirm Assisstant

Use this service to confirm or decline event assisstance.

#### Request

* URL: /v1.0/student/{student_id}/event/{event_id}/confirm_assisstant
* Method: POST
* Body:

``` json
{
    "requestContent": {
        "confirmed": true
    }
}
```

| Key | Description | Type | Rules |
|-----|-------------|------|-------|
| requestContent | Request data | Object | (Required) |
| requestContent.confirmed | Confirm assist to event | Bool | (Required) |

#### Response

* HTTP Status: 200 (Ok)
* Body:

``` json
{
    "info": {
        "type": "success",
        "sessionId": "gTfI0uOuSZzl4d2nA4no5PIqrktzRgXu..."
    }
}
```

[Return](#ConfirmAssisstant)


< Back to [Home](../home.md)
