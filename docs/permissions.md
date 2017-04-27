Permissions are the ability to access an action within the app. Every permission corresponds to an API call from our REST API.
Don't feel intimidated by the following table, for most users the default roles and permissions will be suitable. This information is here if you do wish to modify your roles.

| Permission Name    |   Description  |
| ------------- |:-------------:|
| get_users | Gets all Users |
| get_users_own | Gets the User object of the requester |
| get_users_search | Gets all Users by search |
| get_users_id | Gets all Users |
| put_users_id | Updates a User |
| delete_users_id | Deletes a User |
| get_users_id_avatar | Gets User Avatar |
| put_users_id_avatar | Adds a User Avatar |
| post_users_register | Registers a new User |
| post_users_id_suspend | Suspend the User |
| post_users_invite | Invites a new User |
| get_funds | Gets all funds |
| post_funds | Create new fund |
| get_funds_own | Gets users own funds |
| get_funds_search | Gets all funds by search |
| get_funds_id | Gets fund |
| put_funds_id | Updates a fund |
| get_roles | Gets all roles |
| post_roles | Create new role |
| get_roles_search | Gets all roles by search |
| get_roles_id | Gets all roles |
| put_roles_id | Updates a role |
| delete_roles_id | Deletes a role |
| get_roles_manage_permissions | Gets all roles with permissions |
| post_roles_manage_permissions | Update role with permission |
| get_service_templates | Gets all service-templates |
| post_service_templates | Create new service-template |
| get_service_templates_public | Gets all public service-templates |
| get_service_templates_search | Gets all service-templates by search |
| get_service_templates_id | Gets all service-templates |
| put_service_templates_id | Updates a service_templates |
| delete_service_templates_id | Deletes a service-template |
| get_service_templates_id_icon | Gets Service Template Icon |
| put_service_templates_id_icon | Adds a Service Template Icon |
| get_service_templates_id_image | Gets Service Template Image |
| put_service_templates_id_image | Adds a Service Template Image |
| get_service_templates_id_request | Gets a service-template Request |
| put_service_templates_id_request | Requests a service-instance |
| get_service_categories | Gets all service-categories |
| post_service_categories | Create new service-category |
| get_service_categories_search | Gets all service-categories by search |
| get_service_categories_id | Gets all service-categories |
| put_service_categories_id | Updates a service-category |
| delete_service_categories_id | Deletes a service-category |
| get_service_template_properties | Gets all service-template-properties |
| post_service_template_properties | Create new service-template-property |
| get_service_template_properties_search | Gets all service-template-properties by search |
| get_service_template_properties_id | Gets all service-template-properties |
| put_service_template_properties_id | Updates a service-template-property |
| delete_service_template_properties_id | Deletes a service-template-property |
| get_service_instances | Gets all service-instances |
| get_service_instances_own | Gets all service-instances owned by user |
| get_service_instances_search | Gets all service-instances by search |
| get_service_instances_id | Get a service-instance by id |
| put_service_instances_id | Updates a service-instance |
| delete_service_instances_id | Deletes a service-instance |
| post_service_instances_id_approve | Approves a service-instance |
| post_service_instances_id_change_price | Approves a service-instance |
| post_service_instances_id_cancel | Cancel a service-instance |
| post_service_instances_id_request_cancellation | Request Cancellation of a service-instance |
| post_service_instances_id_add_charge | Add a charge to a service-instance |
| get_service_instances_id_awaiting_charges | Get service-instance awaiting charges |
| post_service_instances_id_approve_charges | Approve a service-instance charges |
| post_service_instances_id_files | Add a service-instance Files |
| get_service_instances_id_files | Get service-instance files |
| delete_service_instances_id_files_fid | Add a service-instance Files |
| get_service_instances_id_files_fid | Get service-instance files |
| get_service_instance_properties | Gets all service-instance-properties |
| post_service_instance_properties | Create newservice-instance-properties |
| get_service_instance_properties_search | Gets all service-instance-properties by search |
| get_service_instance_properties_id | Gets all service-instance-properties |
| put_service_instance_properties_id | Updates aservice-instance-properties |
| delete_service_instance_properties_id | Deletes aservice-instance-properties |
| get_service_instance_messages | Gets all service-instance-messages |
| post_service_instance_messages | Create newservice-instance-messages |
| get_service_instance_messages_search | Gets all service-instance-messages by search |
| get_service_instance_messages_id | Gets all service-instance-messages |
| put_service_instance_messages_id | Updates aservice-instance-messages |
| delete_service_instance_messages_id | Deletes aservice-instance-messages |
| get_service_instance_cancellations | Gets all service-instance-cancellations |
| post_service_instance_cancellations | Create new service-instance-cancellations |
| get_service_instance_cancellations_own | Gets all service-instance-cancellations owned by user |
| get_service_instance_cancellations_search | Gets all service-instance-cancellations by search |
| get_service_instance_cancellations_id | Gets all service-instance-cancellations |
| put_service_instance_cancellations_id | Updates a service-instance-cancellation |
| delete_service_instance_cancellations_id | Deletes a service-instance-cancellation |
| post_service_instance_cancellations_id_approve | Approves a service-instance-cancellations |
| post_service_instance_cancellations_id_reject | Rejects a service-instance-cancellations |
| post_service_instance_cancellations_id_undo | Rejects a service-instance-cancellations for the user who created it |
| get_event_logs | Gets all Event Logs |
| post_event_logs | Create new Event Log |
| get_event_logs_search | Gets all Event Logs by search |
| get_event_logs_id | Gets all Event Logs |
| put_event_logs_id | Updates a Event Log |
| delete_event_logs_id | Deletes a Event Log |
| get_email_templates | Gets all Email Templates |
| post_email_templates | Create new Email Template |
| get_email_templates_search | Gets all Email Templates by search |
| get_email_templates_id | Gets all Email Templates |
| put_email_templates_id | Updates a Email Template |
| delete_email_templates_id | Deletes a Email Template |
| get_email_templates_id_roles | Gets Email Template Roles |
| put_email_templates_id_roles | Updates an Email Template Role |
| get_invoices | Gets all Invoices |
| get_invoices_own | Gets all Invoices owned by user |
| get_invoices_search | Gets all Invoices by search |
| get_invoices_id | Gets all Invoices |
| get_invoices_upcoming_id | Gets upcoming Invoices |
| post_invoices_id_refund | Performs refund on Invoice |
| get_system_options | Gets all System Options |
| put_system_options | Batch Updates System Options |
| get_system_options_public | Gets all public System Options |
| get_system_options_id | Gets a System Option |
| put_system_options_id | Updates a System Option |
| get_system_options_file_id | Gets a System File Options |
| put_system_options_file_id | Updates a System Option |
| post_charge_id_approve | Approves a Charge Item |
| post_charge_id_cancel | Cancels a Charge Item |
| post_auth_token | Gets a Authorization Token |
| post_auth_session_clear | Clears session |
| post_auth_reset_password | Send Reset password email |
| get_auth_reset_password_uid_token | Get User password reset token |
| post_auth_reset_password_uid_token | Reset user password |
| get_analytics_data | Gets Analytics Data |
| get_analytics_properties_id | Gets all instance properties based on template id |
| get_permissions | Gets all permissions |
| post_stripe_preconfigure | First call to make to change stripe keys |
| post_stripe_reconfigure | Second call to make to change stripe keys |
| get_stripe_keys | Gets stripe keys |