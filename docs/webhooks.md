# Managing Webhooks


## Pre-Provision
#### Description
This hook is called when a customer first requests a service instance, this stage is good for validation of parameters, logging, and CMDB integration actions such as creating a configuration item.
#### Triggered By
Calling [Requesting Service Instance](https://api-docs.servicebot.io/#operation--service-templates--id--request-post)
#### Example Payload
```json
{
  "event_name": "pre_provision",
  "event_data": {
    "request": {
      "id": 1,
      "category_id": 1,
      "created_by": 1,
      "name": "MySaaS",
      "description": "MySaaS Super Offering, does everything",
      "details": "<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque sed luctus sapien, sit amet scelerisque ante. Vivamus nec mauris lacinia lectus ornare fringilla. Nunc vulputate purus vehicula, convallis diam sit amet, pellentesque mauris. Mauris a justo condimentum, ultricies arcu a, tincidunt eros. Phasellus maximus vulputate elit a pharetra. Integer vestibulum tincidunt magna. Sed consequat ornare finibus. Maecenas ut sem id justo rutrum rutrum in at justo. Aliquam at libero ut orci maximus pharetra. Etiam a urna non ante ultricies posuere. Vivamus ornare augue quis eros ultricies, vitae accumsan dolor fermentum. Sed rutrum urna ac erat cursus tincidunt. Proin fermentum justo dui, fermentum rutrum libero porttitor ut. Aliquam et ligula leo. Proin dui nisi, tempor non eleifend quis, ultricies et risus.</p>",
      "published": true,
      "statement_descriptor": "asd",
      "trial_period_days": 14,
      "amount": 5000,
      "currency": "usd",
      "interval": "month",
      "interval_count": 1,
      "type": "subscription",
      "subscription_prorate": true,
      "split_configuration": null,
      "created_at": "2018-03-28T15:09:10.686Z",
      "updated_at": "2018-03-28T15:09:10.686Z",
      "references": {
        "service_template_properties": [
          {
            "id": 1,
            "name": "premium",
            "type": "checkbox",
            "data": {
              "value": true
            },
            "config": {
              "pricing": {
                "value": 2000,
                "operation": "add"
              }
            },
            "prop_class": null,
            "prop_label": "Premium",
            "prop_description": null,
            "created_at": "2018-03-28T15:09:10.708Z",
            "updated_at": "2018-03-28T15:09:10.708Z",
            "parent_id": 1,
            "private": false,
            "prompt_user": true,
            "required": false
          },
          {
            "id": 2,
            "name": "business-name",
            "type": "text",
            "data": {
              "value": "Test Industries"
            },
            "config": {},
            "prop_class": null,
            "prop_label": "Business Name",
            "prop_description": null,
            "created_at": "2018-03-28T15:09:10.708Z",
            "updated_at": "2018-03-28T15:09:10.708Z",
            "parent_id": 1,
            "private": false,
            "prompt_user": true,
            "required": true
          }
        ]
      },
      "email": "customer@test.com"
    },
    "template": {
        "id": 1,
        "category_id": 1,
        "created_by": 1,
        "name": "MySaaS",
        "description": "MySaaS Super Offering, does everything",
        "details": "<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque sed luctus sapien, sit amet scelerisque ante. Vivamus nec mauris lacinia lectus ornare fringilla. Nunc vulputate purus vehicula, convallis diam sit amet, pellentesque mauris. Mauris a justo condimentum, ultricies arcu a, tincidunt eros. Phasellus maximus vulputate elit a pharetra. Integer vestibulum tincidunt magna. Sed consequat ornare finibus. Maecenas ut sem id justo rutrum rutrum in at justo. Aliquam at libero ut orci maximus pharetra. Etiam a urna non ante ultricies posuere. Vivamus ornare augue quis eros ultricies, vitae accumsan dolor fermentum. Sed rutrum urna ac erat cursus tincidunt. Proin fermentum justo dui, fermentum rutrum libero porttitor ut. Aliquam et ligula leo. Proin dui nisi, tempor non eleifend quis, ultricies et risus.</p>",
        "published": true,
        "statement_descriptor": "asd",
        "trial_period_days": 14,
        "amount": 5000,
        "overhead": null,
        "currency": "usd",
        "interval": "month",
        "interval_count": 1,
        "type": "subscription",
        "subscription_prorate": true,
        "split_configuration": null,
        "created_at": "2018-03-28T15:09:10.686Z",
        "updated_at": "2018-03-28T15:09:10.686Z"
    }
  }
}
```
## Post-Provision
#### Description
In this stage, the service instance finished being created. This is a good hook to listen to if you need to give a user access to your app, or alert third party integrations such as sending a Slack message.
#### Triggered By
Completion of [requesting Service Instance](https://api-docs.servicebot.io/#operation--service-templates--id--request-post)
#### Example Payload
```json
{
  "event_name": "post_provision",
  "event_data": {
    "request": {
      "id": 1,
      "category_id": 1,
      "created_by": 1,
      "name": "MySaaS",
      "description": "MySaaS Super Offering, does everything",
      "details": "<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque sed luctus sapien, sit amet scelerisque ante. Vivamus nec mauris lacinia lectus ornare fringilla. Nunc vulputate purus vehicula, convallis diam sit amet, pellentesque mauris. Mauris a justo condimentum, ultricies arcu a, tincidunt eros. Phasellus maximus vulputate elit a pharetra. Integer vestibulum tincidunt magna. Sed consequat ornare finibus. Maecenas ut sem id justo rutrum rutrum in at justo. Aliquam at libero ut orci maximus pharetra. Etiam a urna non ante ultricies posuere. Vivamus ornare augue quis eros ultricies, vitae accumsan dolor fermentum. Sed rutrum urna ac erat cursus tincidunt. Proin fermentum justo dui, fermentum rutrum libero porttitor ut. Aliquam et ligula leo. Proin dui nisi, tempor non eleifend quis, ultricies et risus.</p>",
      "published": true,
      "statement_descriptor": "asd",
      "trial_period_days": 14,
      "amount": 7000,
      "currency": "usd",
      "interval": "month",
      "interval_count": 1,
      "type": "subscription",
      "subscription_prorate": true,
      "split_configuration": null,
      "created_at": "2018-03-28T15:09:10.686Z",
      "updated_at": "2018-03-28T15:09:10.686Z",
      "references": {
        "service_template_properties": [
          {
            "id": 1,
            "name": "premium",
            "type": "checkbox",
            "data": {
              "value": true
            },
            "config": {
              "pricing": {
                "value": 2000,
                "operation": "add"
              }
            },
            "prop_class": null,
            "prop_label": "Premium",
            "prop_description": null,
            "created_at": "2018-03-28T15:09:10.708Z",
            "updated_at": "2018-03-28T15:09:10.708Z",
            "parent_id": 1,
            "private": false,
            "prompt_user": true,
            "required": false
          },
          {
            "id": 2,
            "name": "business-name",
            "type": "text",
            "data": {
              "value": "Test Industries"
            },
            "config": {},
            "prop_class": null,
            "prop_label": "Business Name",
            "prop_description": null,
            "created_at": "2018-03-28T15:09:10.708Z",
            "updated_at": "2018-03-28T15:09:10.708Z",
            "parent_id": 1,
            "private": false,
            "prompt_user": true,
            "required": true
          }
        ]
      },
      "email": "customer@test.com"
    },
    "template": {
        "id": 1,
        "category_id": 1,
        "created_by": 1,
        "name": "MySaaS",
        "description": "MySaaS Super Offering, does everything",
        "details": "<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque sed luctus sapien, sit amet scelerisque ante. Vivamus nec mauris lacinia lectus ornare fringilla. Nunc vulputate purus vehicula, convallis diam sit amet, pellentesque mauris. Mauris a justo condimentum, ultricies arcu a, tincidunt eros. Phasellus maximus vulputate elit a pharetra. Integer vestibulum tincidunt magna. Sed consequat ornare finibus. Maecenas ut sem id justo rutrum rutrum in at justo. Aliquam at libero ut orci maximus pharetra. Etiam a urna non ante ultricies posuere. Vivamus ornare augue quis eros ultricies, vitae accumsan dolor fermentum. Sed rutrum urna ac erat cursus tincidunt. Proin fermentum justo dui, fermentum rutrum libero porttitor ut. Aliquam et ligula leo. Proin dui nisi, tempor non eleifend quis, ultricies et risus.</p>",
        "published": true,
        "statement_descriptor": "asd",
        "trial_period_days": 14,
        "amount": 5000,
        "overhead": null,
        "currency": "usd",
        "interval": "month",
        "interval_count": 1,
        "type": "subscription",
        "subscription_prorate": true,
        "split_configuration": null,
        "created_at": "2018-03-28T15:09:10.686Z",
        "updated_at": "2018-03-28T15:09:10.686Z"
    },
    "instance": {
        "id": 1,
        "service_id": 1,
        "user_id": 2,
        "requested_by": 2,
        "payment_plan": {
          "id": "MySaaS-ID1-zy9g",
          "object": "plan",
          "amount": 7000,
          "created": 1522249800,
          "currency": "usd",
          "interval": "month",
          "interval_count": 1,
          "livemode": false,
          "metadata": {},
          "nickname": null,
          "product": "prod_CZpZewO8rjMIhN",
          "trial_period_days": 14,
          "statement_descriptor": "asd",
          "name": "MySaaS"
        },
        "name": "MySaaS",
        "description": "MySaaS Super Offering, does everything",
        "subscription_id": "sub_CZpZ8aABmUjBxk",
        "subscribed_at": 1522249801,
        "trial_end": 1523459401,
        "status": "running",
        "type": "subscription",
        "split_configuration": null,
        "created_at": "2018-03-28T15:09:57.818Z",
        "updated_at": "2018-03-28T15:09:59.828Z"
    }
  }
}
```
## Pre-Property-Change
#### Description
The stage before a property change occurs, in this step you can see the instance and the updates to the properties.
#### Triggered By
[Changing the properties](https://api-docs.servicebot.io/#operation--service-instances--id--change-properties-post) on a Service Instance
#### Example Payload
```json
{
  "event_name": "pre_property_change",
  "event_data": {
    "instance": {
      "id": 1,
      "service_id": 1,
      "user_id": 2,
      "requested_by": 2,
      "payment_plan": {
        "id": "MySaaS-ID1-secn",
        "name": "MySaaS",
        "tiers": null,
        "amount": 7000,
        "object": "plan",
        "created": 1522423618,
        "product": "prod_CaaIL3fbRtJJbq",
        "currency": "usd",
        "interval": "month",
        "livemode": false,
        "metadata": {},
        "nickname": null,
        "tiers_mode": null,
        "usage_type": "licensed",
        "billing_scheme": "per_unit",
        "interval_count": 1,
        "transform_usage": null,
        "trial_period_days": null,
        "statement_descriptor": "asd"
      },
      "name": "MySaaS",
      "description": "MySaaS Super Offering, does everything",
      "subscription_id": "sub_CZpZ8aABmUjBxk",
      "subscribed_at": "1522249801",
      "trial_end": null,
      "status": "running",
      "type": "subscription",
      "split_configuration": null,
      "created_at": "2018-03-28T15:09:57.818Z",
      "updated_at": "2018-03-30T15:26:56.343Z",
      "references": {
        "service_instance_messages": [],
        "service_instance_properties": [
          {
            "id": 1,
            "name": "premium",
            "type": "checkbox",
            "data": {
              "value": true
            },
            "config": {
              "pricing": {
                "value": 2000,
                "operation": "add"
              }
            },
            "prop_class": null,
            "prop_label": "Premium",
            "prop_description": null,
            "created_at": "2018-03-28T15:09:10.708Z",
            "updated_at": "2018-03-28T15:09:10.708Z",
            "parent_id": 1,
            "private": false,
            "prompt_user": true,
            "required": false
          },
          {
            "id": 2,
            "name": "business-name",
            "type": "text",
            "data": {
              "value": "GreatCompany"
            },
            "config": {},
            "prop_class": null,
            "prop_label": "Business Name",
            "prop_description": null,
            "created_at": "2018-03-28T15:09:10.708Z",
            "updated_at": "2018-03-28T15:09:10.708Z",
            "parent_id": 1,
            "private": false,
            "prompt_user": true,
            "required": false
          }
        ],
        "users": [
          {
            "id": 2,
            "role_id": 3,
            "name": null,
            "email": "customer@test.com",
            "provider": "local",
            "status": "invited",
            "customer_id": "cus_CZpZrA96UGKecK",
            "phone": null,
            "last_login": null,
            "created_at": "2018-03-28T15:09:57.779Z",
            "updated_at": "2018-03-28T15:09:57.779Z"
          }
        ],
        "service_instance_cancellations": [],
        "charge_items": []
      }
    },
    "property_updates": [
      {
        "id": 1,
        "name": "premium",
        "type": "checkbox",
        "data": {
          "value": false
        },
        "config": {
          "pricing": {
            "value": 2000,
            "operation": "add"
          }
        },
        "prop_class": null,
        "prop_label": "Premium",
        "prop_description": null,
        "created_at": "2018-03-28T15:09:10.708Z",
        "updated_at": "2018-03-28T15:09:10.708Z",
        "parent_id": 1,
        "private": false,
        "prompt_user": true,
        "required": false
      },
      {
        "id": 2,
        "name": "business-name",
        "type": "text",
        "data": {
          "value": "CoolCompany"
        },
        "config": {},
        "prop_class": null,
        "prop_label": "Business Name",
        "prop_description": null,
        "created_at": "2018-03-28T15:09:10.708Z",
        "updated_at": "2018-03-28T15:09:10.708Z",
        "parent_id": 1,
        "private": false,
        "prompt_user": true,
        "required": false
      }
    ]
  }
}
```
## Post-Property-Change
#### Description
Called after a property change occurrs, the `instance` will reflect any possible price changes which may have occurred. This is good for detecting when a customer changes their "tier" for example changing to a premium subscription from a basic.
#### Triggered By
Completion of a [property change](https://api-docs.servicebot.io/#operation--service-instances--id--change-properties-post)
#### Example Payload
```json
{
  "event_name": "post_property_change",
  "event_data": {
    "instance": {
      "id": 1,
      "service_id": 1,
      "user_id": 2,
      "requested_by": 2,
      "payment_plan": {
        "id": "MySaaS-ID1-k0n7",
        "name": "MySaaS",
        "tiers": null,
        "amount": 5000,
        "object": "plan",
        "created": 1522423730,
        "product": "prod_CaaKnqpZx23KYL",
        "currency": "usd",
        "interval": "month",
        "livemode": false,
        "metadata": {},
        "nickname": null,
        "tiers_mode": null,
        "usage_type": "licensed",
        "billing_scheme": "per_unit",
        "interval_count": 1,
        "transform_usage": null,
        "trial_period_days": null,
        "statement_descriptor": "asd"
      },
      "name": "MySaaS",
      "description": "MySaaS Super Offering, does everything",
      "subscription_id": "sub_CZpZ8aABmUjBxk",
      "subscribed_at": "1522249801",
      "trial_end": null,
      "status": "running",
      "type": "subscription",
      "split_configuration": null,
      "created_at": "2018-03-28T15:09:57.818Z",
      "updated_at": "2018-03-30T15:28:48.474Z",
      "references": {
        "service_instance_properties": [
          {
            "id": 1,
            "name": "premium",
            "type": "checkbox",
            "data": {
              "value": false
            },
            "config": {
              "pricing": {
                "value": 2000,
                "operation": "add"
              }
            },
            "prop_class": null,
            "prop_label": "Premium",
            "prop_description": null,
            "created_at": "2018-03-28T15:09:10.708Z",
            "updated_at": "2018-03-28T15:09:10.708Z",
            "parent_id": 1,
            "private": false,
            "prompt_user": true,
            "required": false
          },
          {
            "id": 2,
            "name": "business-name",
            "type": "text",
            "data": {
              "value": "CoolCompany"
            },
            "config": {},
            "prop_class": null,
            "prop_label": "Business Name",
            "prop_description": null,
            "created_at": "2018-03-28T15:09:10.708Z",
            "updated_at": "2018-03-28T15:09:10.708Z",
            "parent_id": 1,
            "private": false,
            "prompt_user": true,
            "required": false
          }
        ],
        "service_instance_messages": [],
        "users": [
          {
            "id": 2,
            "role_id": 3,
            "name": null,
            "email": "customer@test.com",
            "provider": "local",
            "status": "invited",
            "customer_id": "cus_CZpZrA96UGKecK",
            "phone": null,
            "last_login": null,
            "created_at": "2018-03-28T15:09:57.779Z",
            "updated_at": "2018-03-28T15:09:57.779Z"
          }
        ],
        "service_instance_cancellations": [],
        "charge_items": []
      }
    }
  }
}
```
## Pre-Cancellation
#### Description
#### Triggered By
#### Example Payload
## Post-Cancellation
#### Description
#### Triggered By
#### Example Payload
## Pre-Resubscribe
#### Description
#### Triggered By
#### Example Payload
## Post-Resubscribe
#### Description
#### Triggered By
#### Example Payload
