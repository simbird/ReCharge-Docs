## The Widget

This is the **ReCharge Widget**, embedded by ReCharge Payments on all stores at installation. It's broken down into 3 main components: **Purchase options**, **Delivery intervals**, and **Help**.

![Subscription Widget](http://host.coreycapetillo.com/github/widget-v3-widget.png)

**Purchase options** let the customer choose between purchasing the item once, or signing up for a subscription service for recurring item delivery.

**Delivery intervals** are based on delivery type: either days, weeks or months. The store owner determines the available options, which are then made available for customers so they may adjust the subscription service to their needs.

**Help** is provided via the tooltip that appears beneath the widget, allowing curious customers to find out more about how subscription services work and how to obtain more information when they've got a problem.

## Features

- **No jQuery** We are using only vanilla JavaScript
- **Cross-browser support** Microsoft IE 9+, Chrome 53+, Safari 9+, Firefox 49+, Opera 40+
- **Disable page caching** If page is loaded from cache (browser back/forward button), force a page reload.

## Embed Code

```javascript
var myProduct = {
	id: {{ product.id }},
	subscription_id: {{ subscription_id }},
	shop_currency: "{{ shop.currency }}",
	currency_prefix: "{{ currency_prefix }}",
	currency_suffix: "{{ currency_suffix }}",
	subscription_only: {{ subscription_only }},
	select_subscription_first: {{ select_subscription_first }},
	shipping_interval_unit_type: "{{ shipping_interval_unit_type }}",
	shipping_interval_frequency: [{% for interval in shipping_interval_frequency %}{{ interval }}, {% endfor %}],
	discount_percentage: {{ discount_percentage }},
	variant_to_duplicate: { {% for variant in product.variants %}{{ variant.id }}:'{{ variant.metafields.subscriptions.discount_variant_id }}', {% endfor %} },
	variant_to_price: { {% for variant in product.variants %}{{ variant.id }}:'{{ variant.price }}', {% endfor %} },
	duplicate_to_price: { {% for variant in product.variants %}{{ variant.metafields.subscriptions.discount_variant_id }}: '{{ variant.metafields.subscriptions.discount_variant_price | replace: ".", "" }}', {% endfor %} },
};
```

## Customization

| Option | Type | Default | Description |
|:--|:--|:--|:--|
| `id` | Integer | `{{ product.id }}` | We use Shopify liquid to provide the id for the active product. |
| `subscription_id` | Integer | `{{ subscription_id }}` | The subscription ID is stored via a product meta tag and retried using Shopify liquid. |
| `subscription_only` | Boolean | `false` | If set to `true`, the "One-time purchase" option will be hidden, discounts will be disabled, and the widget will only be visible if 2 or more delivery options are available. |
| `select_subscription_first` | Boolean | `false` | If set to `true`, the subscription option will be pre-selected. |
| `default_purchase_type` | String | `"onetime"` | If set to `"autodeliver"`, the subscription option will be pre-selected. |
| `shipping_interval_frequency` | Array, Integer | 30 | Pairs with `shipping_interval_unit_type` to build the delivery option selector |
| `currency_prefix` | String | `"$"` | The default symbol is dependant on the currency settings on the Shopify store when ReCharge is installed. |
| `currency_suffix` | String | `""` | Can be used to customize the price further, such as adding " USD". |
| `discount_percentage` | Integer | `0` | If greater than 0, labels will show the pricing adjustments and price updaters will be used |
| `label_onetime` | String | `"One-time purchase"` | Label for the single-purchase option. |
| `label_autodeliver` | String | `"Subscribe &amp; save"` | Label for the subscription option |
| `label_deliver_every` | String | `"Deliver every"` | Label for the interval selector |


### Style Notes:
```
	#rc_container {
		width: 100%;
		disable flex
		display block;
	}
```