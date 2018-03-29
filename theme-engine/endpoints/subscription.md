Data objects available are limited by endpoint. Double-check your URL if a certain set of data isn't available.

#### Directory
* [subscriptions](#subscriptions)
* [subscription](#subscription)
* [subscription_activate](#subscription_activate)
* [subscription_cancel](#subscription_cancel)
* [subscription_edit](#subscription_edit)
* [subscription_new](#subscription_new)
* [subscription_charge_date](#subscription_charge_date)

---

## subscriptions
List all subscriptions for the current customer.

**URL:** `{{ list_subscriptions_url }}`

**Route:** `/tools/recurring/customer_portal/<string:customer_hash>/subscriptions`

**Template file:** `subscriptions.html`

#### Available objects
* [Store](https://github.com/SocalProofit/customcheckout/wiki/Store-object)
* [Translation](https://github.com/SocalProofit/customcheckout/wiki/Translation-object)
* [Customer](https://github.com/SocalProofit/customcheckout/wiki/Customer-object)
* [Addresses](https://github.com/SocalProofit/customcheckout/wiki/Address-object)
* [Subscriptions](https://github.com/SocalProofit/customcheckout/wiki/Subscription-object)

---

## subscription
Show details for the current subscription.

**URL:** `{{ subscription | show_subscription_url }}` or `{{ subscription.id | show_subscription_url }}`

**Route:** `/tools/recurring/customer_portal/<string:customer_hash>/subscriptions/<int:subscription_id>`

**Template file:** `subscription.html`

#### Available objects
* [Store](https://github.com/SocalProofit/customcheckout/wiki/Store-object)
* [Translation](https://github.com/SocalProofit/customcheckout/wiki/Translation-object)
* [Customer](https://github.com/SocalProofit/customcheckout/wiki/Customer-object)
* [Subscription](https://github.com/SocalProofit/customcheckout/wiki/Subscription-object)
* [Ruleset](https://github.com/SocalProofit/customcheckout/wiki/Ruleset-object)
* [Variants](https://github.com/SocalProofit/customcheckout/wiki/Variant-object)

---

## subscription_activate
Activate or re-activate the current subscription

**URL:** `{{ subscription | subscription_activate_url }}` or `{{ subscription.id | subscription_activate_url }}`

**Route:** `/tools/recurring/customer_portal/<string:customer_hash>/subscriptions/<int:subscription_id>/activate`

**Template file:** `subscription_activate.html`

#### Available objects
* [Store](https://github.com/SocalProofit/customcheckout/wiki/Store-object)
* [Translation](https://github.com/SocalProofit/customcheckout/wiki/Translation-object)
* [Customer](https://github.com/SocalProofit/customcheckout/wiki/Customer-object)
* [Subscription](https://github.com/SocalProofit/customcheckout/wiki/Subscription-object)
* [Ruleset](https://github.com/SocalProofit/customcheckout/wiki/Ruleset-object)
* [Variants](https://github.com/SocalProofit/customcheckout/wiki/Variant-object)

---

## subscription_cancel
Cancel the current subscription.

**URL:** `{{ subscription | cancel_subscription_url }}` or `{{ subscription.id | cancel_subscription_url }}`

**Route:** `/tools/recurring/customer_portal/<string:customer_hash>/subscriptions/<int:subscription_id>/cancel`

**Template file:** `subscription_cancel.html`

#### Available objects
* [Store](https://github.com/SocalProofit/customcheckout/wiki/Store-object)
* [Translation](https://github.com/SocalProofit/customcheckout/wiki/Translation-object)
* [Customer](https://github.com/SocalProofit/customcheckout/wiki/Customer-object)
* [Subscription](https://github.com/SocalProofit/customcheckout/wiki/Subscription-object)
* [Ruleset](https://github.com/SocalProofit/customcheckout/wiki/Ruleset-object)
* [Variants](https://github.com/SocalProofit/customcheckout/wiki/Variant-object)

---

## subscription_edit
Edit the properties of the current subscription.

**URL:** `{{ subscription | update_subscription_url }}` or `{{ subscription.id | update_subscription_url }}`

**Route:** `/tools/recurring/customer_portal/<string:customer_hash>/subscriptions/<int:subscription_id>/edit`

**Template file:** `address_edit.html`

#### Available objects
* [Store](https://github.com/SocalProofit/customcheckout/wiki/Store-object)
* [Translation](https://github.com/SocalProofit/customcheckout/wiki/Translation-object)
* [Customer](https://github.com/SocalProofit/customcheckout/wiki/Customer-object)
* [Subscriptions](https://github.com/SocalProofit/customcheckout/wiki/Subscription-object)
* [Ruleset](https://github.com/SocalProofit/customcheckout/wiki/Ruleset-object)
* [Variants](https://github.com/SocalProofit/customcheckout/wiki/Variant-object)

---

## subscription_new
A form to create a new subscription for the current customer.

**URL:** `{{ create_subscription_url }}`

**Route:** `/tools/recurring/customer_portal/<string:customer_hash>/subscriptions/new`

**Template file:** `subscription_new.html`

#### Available objects
* [Store](https://github.com/SocalProofit/customcheckout/wiki/Store-object)
* [Translation](https://github.com/SocalProofit/customcheckout/wiki/Translation-object)
* [Customer](https://github.com/SocalProofit/customcheckout/wiki/Customer-object)
* [Address](https://github.com/SocalProofit/customcheckout/wiki/Address-object)
* [Subscriptions](https://github.com/SocalProofit/customcheckout/wiki/Subscription-object)

---

## subscription_charge_date
Set the date of the subscription's next charge.

**URL:** `{{ subscription | subscription_charge_date_url }}` or `{{ subscription.id | subscription_charge_date_url }}`

**Route:** `/tools/recurring/customer_portal/<string:customer_hash>/subscriptions/<int:subscription_id>/change_charge_date`

**Template file:** `subscription_charge_date.html`

#### Available objects
* [Store](https://github.com/SocalProofit/customcheckout/wiki/Store-object)
* [Translation](https://github.com/SocalProofit/customcheckout/wiki/Translation-object)
* [Customer](https://github.com/SocalProofit/customcheckout/wiki/Customer-object)
* [Address](https://github.com/SocalProofit/customcheckout/wiki/Address-object)
* [Subscriptions](https://github.com/SocalProofit/customcheckout/wiki/Subscription-object)