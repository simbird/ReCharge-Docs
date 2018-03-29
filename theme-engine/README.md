Welcome to the ReCharge theme engine documentation pages!

### What is this?

The customer portal is powered by a theme engine which allows you to customize the views to your needs. It is composed of a set of endpoints that provide specific functionality. Each endpoint is associated with a required asset that you can customize to your liking. The endpoint also has a set of objects that can be used to customize the user experience.

### Endpoints
Endpoint are controlled by a route (or URL) and each one is designed to serve a specific purpose. Each one is also tied to a template file, and each template file has access to specific data objects.

* [Customer endpoints](endpoints/customer.md)
* [Address endpoints](endpoints/address.md)
* [Subscription endpoints](endpoints/subscription.md)

### Objects
Data objects provide a way to obtain information, such as a customer's first name or a subscription ID. They're shared and limited by different endpoints/pages. While not every object is available on every page, each page has access to many of the same objects.

* [Address object](objects/address.md)
* [Customer object](objects/customer.md)

### Filters
Filters are useful micro functions used to manipulate data variables on a template. Filters can format text, perform calculations, sort data and more. Not all filters work with every data "type". Some are meant for numbers, while others are used for lists.

* [String filters](filters/strings.md)