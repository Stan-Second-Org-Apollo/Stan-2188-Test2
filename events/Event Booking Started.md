# Event Booking Started

### 

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "Event Booking Started",
    "booking": {
        "ticketList": [
            {
                "event": {
                    "fakeProductId": "<fakeProductId>"
                },
                "price": {
                    "points": "<points>",
                    "sellingPrice": "<sellingPrice>"
                },
                "quantity": "<quantity>"
            }
        ]
    }
});
```

## Variable Definitions

|Field|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|fakeProductId|string|Helper node used by AA Product String Builder to set product to location. This field gets a static value of "event".  With updates to the AA PS extension, this will soon go away.|event|event||||||
|points|integer|Number of points for an item booked or sold.|5000, 2520, 3200|||||||
|quantity|integer|Integer number of products being acted upon \(added to a cart, removed from wishlist, purchased, reserved\)|1, 2, 3, 4, 5||||1|||
|sellingPrice|string|String representation of the price paid after coupons or discounts. Positive. Up to two decimal places for cents. No currency symbol.|200, 29.99, 50, 0|^[0-9]*(\.[0-9]{1,2})?$||||||
