# Order Placed

### 

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "Order Placed",
    "transaction": {
        "item": [
            {
                "altPersonPickUp": "<altPersonPickUp>",
                "pickUpTextNotifications": "<pickUpTextNotifications>",
                "price": {
                    "basePrice": "<basePrice>",
                    "markdownPrice": "<markdownPrice>",
                    "sellingPrice": "<sellingPrice>"
                },
                "productInfo": {
                    "productID": "<productID>"
                },
                "quantity": "<quantity>",
                "shippingCost": "<shippingCost>",
                "shippingVoucherDiscount": "<shippingVoucherDiscount>",
                "tax": "<tax>",
                "voucherDiscount": {
                    "orderLevelDiscountAmount": "<orderLevelDiscountAmount>",
                    "productLevelDiscountAmount": "<productLevelDiscountAmount>"
                }
            }
        ],
        "payment": [
            {
                "paymentAmount": "<paymentAmount>",
                "paymentID": "<paymentID>"
            }
        ],
        "purchaseID": "<purchaseID>",
        "total": {
            "currency": "<currency>"
        }
    }
});
```

## Variable Definitions

|Field|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|altPersonPickUp|integer|When a user has put in the information of an alternate pick up person during the checkout process.||||||||
|basePrice|string|String representation of MSRP of a product. Positive. Up to two decimal places for cents. No currency symbol.|200, 29.99, 50, 0|^[0-9]*(\.[0-9]{1,2})?$||||||
|currency|string|Currency of the transaction. ISO 4217 \(3 character alpha\), uppercase |USD, CAD, GBP, CHF|^[A-Z]{3}$|3|3||||
|markdownPrice|string|String representation of the price offered. Often called 'hard mark' price. Positive. Up to two decimal places for cents. No currency symbol.|200, 29.99, 50, 0|^[0-9]*(\.[0-9]{1,2})?$||||||
|orderLevelDiscountAmount|string|String representation of an order level discount applied to an item in a transaction. Positive. Up to two decimal places for cents. No currency symbol.|5, 20, 10.22, 19.2|^[0-9]*(\.[0-9]{1,2})?$||||||
|paymentAmount|string|String representation of the payment amount. Positive. Up to two decimal places for cents. No currency symbol.|200, 29.99, 50, 0|^[0-9]*(\.[0-9]{1,2})?$||||||
|paymentID|string|Unique identifier of a payment.  Typically an integration key from a back-end system.|ZPH-87698-098|||||||
|pickUpTextNotifications|integer|The count of times a user has selected to receive text notifications during the checkout process.||||||||
|productID|string|Unique Identifier of a product or offering.  Must match the format of back-end systems if used as a key for import of product meta data. Most often, one level above SKU for products with SKU variants. |155, 65588, 987764448|||||||
|productLevelDiscountAmount|string|String representation of product level discount for a transaction. Positive. Up to two decimal places for cents. No currency symbol.|5, 20, 10.22, 19.2|^[0-9]*(\.[0-9]{1,2})?$||||||
|purchaseID|string|Unique identifier of the purchase. Max Length 20. Used as Unique ID of the purchase or deduplication.|ABC-132456789, DEF-132456789, 0987654567|^[a-zA-Z0-9]{6,20}$|6|20||||
|quantity|integer|Integer number of products being acted upon \(added to a cart, removed from wishlist, purchased, reserved\)|1, 2, 3, 4, 5||||1|||
|sellingPrice|string|String representation of the price paid after coupons or discounts. Positive. Up to two decimal places for cents. No currency symbol.|200, 29.99, 50, 0|^[0-9]*(\.[0-9]{1,2})?$||||||
|shippingCost|string|The shipping costs for all items within the shippingGroup of the transaction.|15.05, 2, 0.22, 2.2|^[0-9]*(\.[0-9]{1,2})?$||||||
|shippingVoucherDiscount|string|String representation of an discount applied against shipping costs for a shipping group. Positive. Up to two decimal places for cents. No currency symbol.|5, 20, 10.22, 19.2|^[0-9]*(\.[0-9]{1,2})?$||||||
|tax|string|String representation of the tax collected at a shipment level for a transaction. Positive. Up to two decimal places for cents. No currency symbol.|5.05, 20, 10.22, 9.2|^[0-9]*(\.[0-9]{1,2})?$||||||
