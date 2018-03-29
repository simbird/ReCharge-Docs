Provides essential customer information, as well as associated billing information.

##### Properties

| Property | Liquid | Example output |
| :--- | :--- | :--- |
| **customer.last_name** | `{{ customer.last_name }}` | `Diamond` |
| **customer.first_name** | `{{ customer.first_name }}` | `Dan` |
| **customer.name** | `{{ customer.name }}` | `Dan Diamond` |
| **customer.email** | `{{ customer.email }}` | `dan.diamond@rechargeapps.com` |
| **customer.hash** | `{{ customer.hash }}` | `sadfo8ahwo8asodnas8faosfiasflaksdf` |
| **customer.has\_credit\_card\_purchase** | `{{ customer.has_credit_card_purchase }}` | `True` |
| **customer.shopify\_customer\_id** | `{{ customer.shopify_customer_id }}` | `100399283` |
| **customer.customer\_payment\_type** | `{{ customer.customer_payment_type }}` | `Credit Card` |
| **customer.customer_card** | `{{ customer.customer_card }}` | `3301` |
| **customer.billing_address1** | `{{ customer.billing_address1 }}` | `4141 Celestial Ave` |
| **customer.billing_address2** | `{{ customer.billing_address2 }}` | `Suite 221` |
| **customer.billing_city** | `{{ customer.billing_city }}` | `Santa Monica` |
| **customer.billing_company** | `{{ customer.billing_company }}` | `Super MegaCorp` |
| **customer.billing_country** | `{{ customer.billing_country }}` | `United States` |
| **customer.billing\_first\_name** | `{{ customer.billing_first_name }}` | `Dan` |
| **customer.billing\_last\_name** | `{{ customer.billing_last_name }}` | `Diamond` |
| **customer.billing_zip** | `{{ customer.billing_zip }}` | `90304` |
| **customer.billing_province** | `{{ customer.billing_province }}` | `CA` |