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
### Manage account Embed (Add/update card and cancel/reactivate subscription)

!!! warning "Note"
    This embed will require code to be placed in your server

1. Go to "Integrations"
1. Click on `Embed to allow customers to manage thier account and billing settings`
1. Select your backend language/framework
1. Place the server code in your server
1. Place the client code on the client, and insert the token from the server when a logged in user visits the page
1. Customers can now add/update a funding source and cancel/reactivate their subscriptions using this page
##### Tips
- Using an administrator account, use [this](https://api-docs.servicebot.io/#operation--users--id--token-post) API to get a token for a specific customer
- If your language/framework is not available, you can use a JSON Web Token library to generate a token
