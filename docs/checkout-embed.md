### Checkout Embed

1. Go to "Embeddables -> Checkout"
1. Select the template and plan you would like to embed
1. Copy the HTML given
1. Paste on your existing site where you would like customers to sign up for your subscription
##### Checkout options
In the config for a request embed, these are the options which can customize the embed

| Attribute        | Type           | Description  |
| ------------- |:-------------:| -----|
| templateId      | number | Id of the template you want to embed |
| url      | string      |   URL of your servicebot instance |
| selector | [Element](https://developer.mozilla.org/en-US/docs/Web/API/Element)|  The element you want to turn into a form |
| paymentStructureTemplateId | number | Payment Structure to purchase |
| [handleResponse] | function(response) | a function which gets called after the subscription has been created |
| [forceCard] | boolean | if true, the customer will be prompted to enter credit card in order to request service |
| [propertyOverrides] | Object | Object with keys being property names and values being the value the property will submit with, if these properties are being overriden the customer will not get a chance to fill them out. This is usually used to have an embed for a specific pricing tier, you can find the machine name for a property on the service template edit page |
| [hideSummary] | boolean | if true, the embed will not include a price summary |
| [hideHeaders] | boolean | if true, the embed will not include the service template name and description, only the form |
| [setPassword] | boolean | if true, the customer will be asked to enter a password, which you can use to create their account |
| [redirect] | string | After the subscription has been requested (and after handleResponse if present,) redirect the customer to this location | 
| [email] | string | Set the email field | 
| [token] | string | JSON Web Token for the user you want to make the request with, set this if you want to request subscriptions with existing users |


##### Example Request Config
```javascript
    Servicebot.Checkout({
        templateId : 1,
        paymentStructureTemplateId: 4,
        url : "http://localhost:3000", 
        selector : document.getElementById('servicebot-request-form'),
        handleResponse : async (response) => { //handleResponse can return a promise to be resolved before redirect happens
            await mySaaS.createAccount(response.request.email, response.request.password)
            console.log(response);
        },
        forceCard : false, 
        setPassword: true,
        propertyOverrides : {
            businessName: "MyBiz"
        }
    })
```

##### Tips
- You can add additional javascript logic in the `handleResponse` function
- If you are using synchronous webhooks, any responses from your endpoints will show up in the `handleResponse` payload
