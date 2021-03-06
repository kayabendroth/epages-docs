---
layout: page
key: apps-data-types
title: Data types
---

## address

This object is used for the attributes of shippingAddress and billingAddress.

| Attribute | Type | Description |
| - | :-: |  - |
| company | string | The company of the person associated with the address.|
| salutation | string | The salutation of the customer, e.g. Mr or Mrs.|
| title | string | The academic title of the customer, e.g. professor or PhD.|
| firstName | string | The first name of the person associated with the address.|
| lastName | string | The last name of the person associated with the address.|
| street | string | The street name of the address. |
| streetDetails | string | An additional field for the street address.|
| zipCode | string | The zip or postal code of the address. |
| city | string | The name of the city. |
| state | string | The name of the state.|
| country | string | The name of the country. |
| vatId | string | The Id of the VAT.|
| birthday | string | The date of birth of the person associated with the address. |
| emailAddress | string | The email address of the person associated with the address. |

## attributeSelection

| Attribute | Type | Description |
| - | :-: |  - |
| name | string | The name of the selected product attribute, e.g. colour. |
| value | string | The assigned value of the selected product attribute, e.g. white. |

## basePrice

| Attribute | Type | Description |
| - | :-: |  - |
| refQuantity  | [quantity](page:apps-data-types#quantity) | The standardised unit for the product, e.g. 1 l. |
| refPrice | [price](page:apps-data-types#price) | The price based upon the standardised unit. |
| formatted | string | The formatted output of the base price information, e.g. 1 l = 1.20 EUR. |
| quantity | [quantity](page:apps-data-types#quantity) | The quantity of the product, e.g. 500 ml. |

## cart

| Attribute | Type | Description |
| - | :-: |  - |
| cartid | string | The unique identifier of the cart. |
| billingAddress | [address](page:apps-data-types#address) | The billing address for a cart. |
| shippingAddress | [address](page:apps-data-types#address) | The shipping address for a cart. |
| lineItemContainer | [lineItemContainer](page:apps-data-types#lineitemcontainer) | Contains the line items of a cart. |
| minCartValue | [price](page:apps-data-types#price) | The minimum order value of a shop. |
| checkoutURL | string | The URL that redirects the browser to the merchant’s shop in order to complete the checkout. |

## category

| Attribute | Type | Description |
| - | :-: |  - |
| categoryId | string | The unique identifier of the category a product is assigned to. |
| name | string | The name of the category. |
| pageTitle | string | The title of this category. |
| description | string | The description of the category. |
| specialOffer | boolean | Special offers of this category. |
| images | array of [image](page:apps-data-types#image) | The images belonging to this category. |
| parent | [link](page:apps-data-types#link) | The link to the parent category. |
| subCategories | array of [link] | A list of links to the subcategories. |
| sfUrl | string | The link to the categories in the shop’s storefront. |

## contentPageSummary

| Attribute | Type | Description |
| - | :-: |  - |
| name | string | The name of the content page. |

## customAttribute

| Attribute | Type | Description |
| - | :-: |  - |
| key | string | The identifier of the custom attribute. |
| displayKey | string | The displayed name of the custom attribute. |
| singleValue | boolean | Indicates if just one feature is selected for the custom attribute.  |
| type | enum | The data type of the custom attribute. Can be *string*, *number*, *bool*, *datetime*, *time*, *url*.|
| values | array of [variationValue](page:apps-data-types#variationvalue)| The options selected for the custom attribute. |

## image

This object is used for the attributes of images.

| Attribute | Type | Description |
| - | :-: |  - |
| url | string | The URL of an image. |
| classifier | string | Specifies the image. Can be *Thumbnail*, *Small*, *HotDeal*, *MediumSmall*, *Medium*, *MediumLarge*, *Large*. |

## imageSize

| Attribute | Type | Description |
| - | :-: |  - |
| sizes | array of [image](page:apps-data-types#image) | The size of the images in the slideshow. |

## lineItemContainer

| Attribute | Type | Description |
| - | :-: |  - |
| grandTotal | [price](page:apps-data-types#price) | The total price including product price, shipping and tax. |
| totalBeforeTax | [price](page:apps-data-types#price) | The total price including product price, shipping excluding tax. |
| totalTax | [price](page:apps-data-types#price) | The total amount of the tax. |
| lineItemsSubTotal | [price](page:apps-data-types#price) | The sum of the line item price of all line items. |
| productLineItems | array of [productLineItem](page:apps-data-types#productlineitem) | A list of line items. |
| shippingPrice | [price](page:apps-data-types#price) | The shipping price of the line item. |

## link

This object is used for the attributes of links.

| Attribute | Type | Description |
| - | :-: |  - |
| rel | string | The link relation that describes how the link relates to the call. |
| href | string | The URL of the related link that can be used for subsequent calls. |
| title | string | The title of the item that is linked. (optional)  |

## order

| Attribute | Type | Description |
| - | :-: |  - |
| orderId | string | The unique identifier of the order. |
| orderNumber | string | The order number. |
| creationDate | datetime | The date/time of order placement. Expressed according to ISO 8601. Example: `2015-11-04T08:42:49.000Z` |
| billingAddress | [address](page:apps-data-types#address) | The billing address for the order.  |
| shippingAddress | [address](page:apps-data-types#address) | The shipping address for the order.  |
| invoicedOn | datetime | The date/time the order was invoiced. Expressed according to ISO 8601. Example: `2015-11-04T08:42:49.000Z`   |
| shippedOn | datetime | The date/time the order was shipped. Expressed according to ISO 8601. Example: `2015-11-04T08:42:49.000Z`   |
| pendingOn | datetime | The date/time the order was set to pending. Expressed according to ISO 8601. Example: `2015-11-04T08:42:49.000Z`   |
| archivedOn | datetime | The date/time the order was archived. Expressed according to ISO 8601. Example: `2015-11-04T08:42:49.000Z`   |
| dispatchedOn | datetime | The date/time the order was dispatched. Expressed according to ISO 8601. Example: `2015-11-04T08:42:49.000Z`   |
| viewedOn | datetime | The date/time the order was viewed. Expressed according to ISO 8601. Example: `2015-11-04T08:42:49.000Z`   |
| customerId | string | The unique identifier of the customer.  |
| locale | string | The locale that identifies the origin of the customer.  |
| currencyId | string | The unique identifier of the currency used for payment.  |
| taxModel | string | The taxmodel that applies for the order, e.g. gross.  |
| grandTotal | string | The total cost of the order.  |
| totalBeforeTax | string | The total cost of the order before tax is applied.  |
| comment | string | Internal notes for the order.  |
| cancelledOn | datetime | The date/time the order was cancelled. Expressed according to ISO 8601. Example: `2015-11-04T08:42:49.000Z`  |
| closedOn | datetime | The date/time the order was closed. Expressed according to ISO 8601. Example: `2015-11-04T08:42:49.000Z`  |
| paidOn | datetime | The date/time the order was paid. Expressed according to ISO 8601. Example: `2015-11-04T08:42:49.000Z`  |
| returnedOn | datetime | The date/time the order was returned. Expressed according to ISO 8601. Example: `2015-11-04T08:42:49.000Z`  |
| lineItemContainer | [lineItemContainer](page:apps-data-types#lineitemcontainer) | Contains the line items of an order.  |
| productLineItems | array of [productLineItem](page:apps-data-types#productlineitem) | A list of line items.  |
| shippingPrice | [price](page:apps-data-types#price) | The shipping price for the order.  |
| links | array of [link](page:apps-data-types#link) | The links to the products of the order. |

## price

This object is used for the attributes of basePrice, depositPrice, ecoParticipationPrice, manufacturerPrice, grandTotal, priceWithDeposits, totalBeforeTax, totalTax and lineItemsSubTotal.

| Attribute | Type | Description |
| - | :-: |  - |
| taxType | string | Indicates if the amount includes tax, e.g. gross. |
| formatted | string | The amount of the price with currency unit. |
| amount | number | The amount of the price. |
| currency | string | The currency code of the price according to ISO 4217. |

## priceInfo

| Attribute | Type | Description |
| - | :-: |  - |
| quantity | [quantity](page:apps-data-types#quantity) | The quantity of the product the price refers to.|
| price | [price](page:apps-data-types#price) | The price of the product.|
| depositPrice | [price](page:apps-data-types#price) | The deposit price for the product, e.g. bottle deposit.|
| ecoParticipationPrice | [price](page:apps-data-types#price) | The advance recycling fee for electric and electronic products which is only in some countries prescribed by law.|
| manufacturerPrice | [price](page:apps-data-types#price) | The sales price recommended by the manufacturer.|
| priceWithDeposits | [price](page:apps-data-types#price) | The price including all deposits, i.e. price, depositPrice and ecoParticipationPrice.|
| basePrice | [basePrice](page:apps-data-types#baseprice) | The price information scaled to a standardised base unit, according to the German base price regulation "Preisangabenverordnung" (PAngV), e.g. 1 l = 1.20 EUR. Is `null` if no reference amount is specified for the product.|

## product

This object is used for the attributes of product.

| Attribute | Type | Description |
| - | :-: |  - |
| productId | string | The unique identifier of the product. |
| name | string | The name of the product. |
| shortDescription | string | Categorises the image, e.g. Thumbnail or Medium. |
| description | string | Categorises the image, e.g. Thumbnail or Medium. |
| priceInfo | object of [priceInfo](page:apps-data-types#priceinfo) | Price information on the product. |
| forSale | boolean | Information on the sale status of the product. Indicates if the product can be added to the shopping basket. |
| specialOffer | boolean | Indicates if the product is a special offer. |
| deliveryWeight | [quantity](page:apps-data-types#quantity) | The delivery weight of the product. |
| shippingMethodsRestrictedTo | array of [link](page:apps-data-types#link) | Information on possible shipping method restrictions, e.g. express delivery only. Can be `null` if no restrictions exist. |
| availabilityText | string | Additional custom information on the product's stock level or the delivery period. |
| availability | enum | The availability of the product. Can be one of *OnStock*, *WarnStock*, *OutStock*. |
| energyLabelsString | string | A list of energy labels applied to this product. Can be one or two values. If two values are returned, the first value is the best energy label, the second is the second-best. |
| energyLabelSourceFile | string | An image or PDF file containing the energy label image supplied by the manufacturer. |
| productDataSheet | string | An image or PDF file containing a datasheet with technical information on the product. Has to be available if the product has an energy label. |
| sfUrl | string | The link to storefront URL of the product. |
| productNumber | string | The product number. |
| manufacturer | string | The manufacturer of the product. |
| upc | string | The Universal Product Code of the product. |
| ean | string | The European Article Number of the product, either EAN-8 or EAN-13. |

## productLineItem

| Attribute | Type | Description |
| - | :-: |  - |
| lineItemId | string | The unique identifier of the line item. |
| sku | string | The stock keeping unit (SKU) corresponding to the line item. |
| name | string | The name of the line item. |
| productId | string | The unique identifier of the product. |
| quantity | [quantity](page:apps-data-types#quantity) | The quantity of the line item. |
| lineItemPrice | [price](page:apps-data-types#price) | The price of the line item. |
| singleItemPrice | [price](page:apps-data-types#price) | The price for a single item. |
| images | array of [image](page:apps-data-types#image) | The image of the line item. |
| links | array of [link](page:apps-data-types#link) | The links to the product line item. |

## productSuggest

| Attribute | Type | Description |
| - | :-: |  - |
| name | string | The name of the product resulting from the query. |
| images | array of [image](page:apps-data-types#image) | The image of the product resulting from the query. |
| link | [link](page:apps-data-types#link) | The link to the product resulting from the query. |

## quantity

This object is used for the attributes of deliveryWeight and quantity.

| Attribute | Type | Description |
| - | :-: |  - |
| amount | decimal | The amount displayed as a numeric value. |
| unit | string | The unit displayed as abbreviated SI unit, if available. Otherwise a localised name if the unit is displayed, e.g. piece(s).  |

## sales

| Attribute | Type | Description |
| - | :-: |  - |
| currency | string | The currency code according to ISO 4217. |
| totalGrossRevenue | number | The total gross revenue received from completed orders.|
| totalNetRevenue | number | The total net revenue received from completed orders.|
| unitsSold | number | The number of sold product units (only available with active filter productId). |
| totalOrders | number | The number of orders for the defined time frame. |

## shippingMethod

| Attribute | Type | Description |
| - | :-: |  - |
| shippingMethodId | string | The unique identifier of the shipping method. |
| name | string | The name of the shipping method.|
| description | string | The description of the shipping method.|
| logo | string | The logo of the shipping method. |

## variation

| Attribute | Type | Description |
| - | :-: |  - |
| link | [link](page:apps-data-types#link)| The link to the product variation. |
| attributeSelection | array of [attributeSelection](page:apps-data-types#attributeselection) | The attribute of the selected product variation. |

## variationAttribute

| Attribute | Type | Description |
| - | :-: |  - |
| name | string | The name of the variation attribute. |
| displayName | string | The displayed name of the variation attribute. |
| values | array of [variationValue](page:apps-data-types#variationvalue) | The values of the variation attribute.  |

## variationValue

| Attribute | Type | Description |
| - | :-: |  - |
| value | string | The key of an attribute, e.g. 004. |
| displayValue | string | The displayed name of the attribute, e.g. XtraLarge. |
