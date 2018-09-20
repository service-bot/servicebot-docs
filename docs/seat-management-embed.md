# Seat Management Embed

!!! warning "Note"
    This embed will require code to be placed in your server

1. Go to "Embeddables"
1. Click on `Seat Management`
1. Select your backend language/framework
1. Place the server code in your server
1. Place the client code on the client, and insert the token from the server when a logged in user visits the page
1. Customers can now add/remove the seats attached to their subscription

## Seat Management options

| Attribute        | Type           | Description  |
| ------------- |:-------------:| -----:|
| url      | string      |   URL of your servicebot instance |
| selector | [Element](https://developer.mozilla.org/en-US/docs/Web/API/Element)|  The element you want to turn into a form |
| token | string | JSON Web Token for the user who owns a service instance you want to manage the seats of|
| [serviceInstanceId] | string | used if the user owns multiple service instances, pass the instance id of the specific instance|

## Example Seat Management Config
```javascript
    Servicebot.SeatManagement({
        url : "https://example.serviceshop.io", 
        selector : document.getElementById('servicebot-seat-management-form'),
        token: "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1aWQiOjMzLCJpYXQiOjE1MzczNzY4MTgsImV4cCI6MTUzNzM4NzYxOH0.yrhyVmzHprR-7b--SpnwaH7ylKjd6q4-isgnm782Q8I"
    })
```

## Tips
- There will be a webhook called everytime a seat is invited
- You should set your invite url in the seat management settings to direct to a page with a login embed
- You can tie a metric based service to seats on edit page for a service
- The invite email can be configured on the `Settings -> Email Settings -> Invite` page
