### Seat Management Embed

1. Go to "Embeddables"
1. Click on `Seat Management`
1. Copy the HTML given
1. Paste on your existing site where you would like a seat management page to be generated
1. Pass a token to the embed for the user you want to manage seats
##### Seat Management options

| Attribute        | Type           | Description  |
| ------------- |:-------------:| -----:|
| url      | string      |   URL of your servicebot instance |
| selector | [Element](https://developer.mozilla.org/en-US/docs/Web/API/Element)|  The element you want to turn into a form |
| token | string | JSON Web Token for the user who owns a service instance you want to manage the seats of|
| [serviceInstanceId] | string | used if the user owns multiple service instances, pass the instance id of the specific instance|

##### Example Seat Management Config
```javascript
    Servicebot.SeatManagement({
        url : "https://example.serviceshop.io", 
        selector : document.getElementById('servicebot-seat-management-form'),
        token: "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1aWQiOjMzLCJpYXQiOjE1MzczNzY4MTgsImV4cCI6MTUzNzM4NzYxOH0.yrhyVmzHprR-7b--SpnwaH7ylKjd6q4-isgnm782Q8I"
    })
```
