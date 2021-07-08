# Event Listing Displayed

### This event is part of the page load sequence, including virtual page loads in the case of single page apps, and must be pushed between the `Page Load Started` and `Page Load Completed` events.

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "Event Listing Displayed",
    "listingDisplayed": {
        "displayCount": "<displayCount>",
        "filterList": "<filterList>",
        "filterListLength": "<filterListLength>",
        "listingContext": "<listingContext>",
        "listingDriver": "<listingDriver>",
        "listingType": "<listingType>",
        "resultsCount": "<resultsCount>",
        "sortDefault": "<sortDefault>",
        "sortOrder": "<sortOrder>"
    }
});
```

## Variable Definitions

|Field|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|displayCount|integer|The total number of items displayed out of all returned items. \(Integer\)|10, 20, 30, 40||||0|||
|filterList|string|A twice delimited string of filterType and filterValue pairs.  Use \~ between type and value.  Use \| between pairs|sort\~price ascending\|color\~green\|size\~medium|||||||
|filterListLength|integer|The number of filterValue pairs in the filterList|0, 20, 12||||0|||
|listingContext|string|Describes the context of a listing display \(sort changed, filter added, filter removed\)|Filter Added, Filter Removed, Sort Change, Pagination|||||||
|listingDriver|string|Describes the action that caused the listing to be displayed|Onsite Search, Curated Assortment, Navigation|||||||
|listingType|string|The type of results being listed|text, product, location, event, room, product location|||||||
|resultsCount|integer|The total number of items returned that matched the search criteria. \(Integer\)|1, 21, 111, 166||||0|||
|sortDefault|integer|The default sort value on listings|A to Z, Low to High, Newest to Oldest||||0|||
|sortOrder|string|Indicates the sort order.|high-low, low-high, nearest-farthest, a-z, newest-oldest|||||||
