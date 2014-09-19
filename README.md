# Drupal Commerce Plaintext Order Summary Tokens

## About this module
Provides tokens that provide plaintext line item summaries suitable for use in order confirmation emails for Drupal Commerce.

The following tokens are provided:

### Product line items:
`[commerce-order:plaintext-product-line-items]`

This produces layout in the following format:

`Product Title - Line Item Label (Qty: Quantity) : Currency CodePrice`

E.g.

Red Widgets - 987676555 (Qty: 3) : GBP60.00

### Shipping line items:
`[commerce-order:plaintext-shipping-line-items]`

This produces layout in the following format:

`Line Item Label (Qty: Quantity) : Currency CodePrice`

E.g.

Ground Shipping (Qty: 1) : GBP10.00

## Frequently Asked Questions

### Can I change the information output?
The output is driven by translatable strings, in the following formats. You can override this with the [string overrides](https://www.drupal.org/project/stringoverrides) module if you wish:

Product line items:

`@product_name - @line_item_label (Qty: @intquantity) : @currency@price`

Shipping line items:

`@line_item_label (Qty: @intquantity) : @currency@price`

### My quantities aren't whole numbers - can I include the exact quantity
Yes - override the template, and use @quantity instead of @intquantity.

### Can I include the currency code instead of the symbol?
Yes. Override the template, and use @currencycode instead of @currency.