# Embedding Servicebot in an existing site/app
You can embed a service template request form or a account management page into any existing website/application

### Request Form Embed

1. Go to "Manage -> Manage Offerings"
1. Click on "Actions -> Embed request form" on the template you would like to embed
1. Copy the HTML given
1. Paste on your existing site where you would like customers to sign up for your subscription
##### Tips
- You can add additional javascript logic in the `handleResponse` function
- if the `forceCard` boolean is true, a credit card input will appear even if there is a free trial
- If you are using synchronous webhooks, any responses from your endpoints will show up in the `handleResponse` payload
### Manage account Embed

!!! warning "Note"
    This embed will require an integration with Servicebot on your server in order to authorize customers securly

1. Integrate your server with Servicebot so you can generate tokens for specific customers in Servicebot (guide coming soon)
1. Paste this HTML on a page which can utilize the generated access tokens
```
  <div id="servicebot-management-form"></div>
  <script src="https://js.stripe.com/v3/"></script>
  <script src="/build/servicebot-embed.js" type="text/javascript"></script>
  <script  type="text/javascript">
    Servicebot.init({
        url : "https://your-servicebot-instance.serviceshop.io",
        selector : document.getElementById('servicebot-management-form'),
        type : "manage",
        token: "{{Server generated user token goes here...}}"
    })
  </script>
```
1. Make sure the `token` field is populated by an authorization token for a specific customer
1. Make sure the `url` is pointing to your Servicebot instance url
1. Customers can now add/update a funding source and cancel/reactivate their subscriptions using this page
##### Tips
- Using an administrator account, use [this](https://api-docs.servicebot.io/#operation--users--id--token-post) API to get a token for a specific customer
