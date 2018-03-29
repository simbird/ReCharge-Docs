Data objects available are limited by endpoint. Double-check your URL if a certain set of data isn't available.

#### Directory
* [addresses](#addresses)
* [address](#address)
* [address_edit](#address_edit)
* [address_new](#address_new)

---

## addresses
List all addresses for the current customer.

**URL:** `{{ list_address_url }}`

**Route:** `/tools/recurring/customer_portal/<string:customer_hash>/addresses`

**Template file:** `addresses.html`

#### Available objects
* [Store](https://github.com/SocalProofit/customcheckout/wiki/Store-object)
* [Translation](https://github.com/SocalProofit/customcheckout/wiki/Translation-object)
* [Customer](https://github.com/SocalProofit/customcheckout/wiki/Customer-object)
* [Address](https://github.com/SocalProofit/customcheckout/wiki/Address-object)
* [Subscriptions](https://github.com/SocalProofit/customcheckout/wiki/Subscription-object)

---

## address
Show details for the current address.

**URL:** `{{ address | show_address_url }}` or `{{ address.id | show_address_url }}`

**Route:** `/tools/recurring/customer_portal/<string:customer_hash>/addresses/<int:address_id>`

**Template file:** `address.html`

#### Available objects
* [Store](https://github.com/SocalProofit/customcheckout/wiki/Store-object)
* [Translation](https://github.com/SocalProofit/customcheckout/wiki/Translation-object)
* [Customer](https://github.com/SocalProofit/customcheckout/wiki/Customer-object)
* [Address](https://github.com/SocalProofit/customcheckout/wiki/Address-object)

---

## address_edit
Form to edit and update the current address.

**URL:** `{{ address | update_address_url }}` or `{{ address.id | update_address_url }}`

**Route:** `/tools/recurring/customer_portal/<string:customer_hash>/addresses/<int:address_id>/edit`

**Template file:** `address_edit.html`

#### Available objects
* [Store](https://github.com/SocalProofit/customcheckout/wiki/Store-object)
* [Translation](https://github.com/SocalProofit/customcheckout/wiki/Translation-object)
* [Customer](https://github.com/SocalProofit/customcheckout/wiki/Customer-object)
* [Address](https://github.com/SocalProofit/customcheckout/wiki/Address-object)

---

## address_new
Page with form to create a new address for current customer.

**URL:** `{{ create_address_url }}`

**Route:** `/tools/recurring/customer_portal/<string:customer_hash>/addresses/new`

**Template file:** `address_new.html`

#### Available objects
* [Store](https://github.com/SocalProofit/customcheckout/wiki/Store-object)
* [Translation](https://github.com/SocalProofit/customcheckout/wiki/Translation-object)
* [Customer](https://github.com/SocalProofit/customcheckout/wiki/Customer-object)
* [Address](https://github.com/SocalProofit/customcheckout/wiki/Address-object)
* [Subscription](https://github.com/SocalProofit/customcheckout/wiki/Subscription-object)