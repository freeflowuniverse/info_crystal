# Crystal Exchange Technical Details

## Tag system

- ```category:value```
- categories are predefined see below, there is a group of volunteers constantly maintaining this system to have optimal efficiency, multiple languages are maintained.

## KIS

- each product/service get's tagged with a one or more categories and predefined values.
- the definition itself is just text and pictures in markdown format.
- This can link any markdown embeddable format (movie, sound, html, ...), so has unlimited flexibility to expose something.

> At first sight this may seem complicated, but its actually very easy and extensible way to define a product, price, ... its much easier than having to work with databases, e-commerce systems, ... <BR>
> the content can be stored in a version controlled system (git) to make it reusable. <BR>
> Its super easy to copy paste & even search/replace.

!!!include:tag_system

### product/service code

- a unique code as created by the manufactor/creator of the branded product/service.
- this code is unique and can only be created by the brand owner.
- example notation ```id:572h```
- it always start ```id:```
- the combination productcode vs brand is unique globally
- this allows a reseller, transporter or manufacturer to locate the right product/service.
- one specific product/service can have multiple codes.

### price definition

- ```price:10:USD```
	- if no unit specified then its per unit sold
	- ```price:10:USD:gram``` this is with a specified unit
- ```currencies:USD,EUR,BTC,TFT```
- ```discount:+10:20%``` , ```discount:+100:30%```
- ```validity:20oct2020-29oct2020```
	- ```validity:-20oct2020``` means till
	- ```validity:+20oct2020``` means from
	- can be combined
	- date format is day in 2 digits, month in 3 letters, year in 4, we use this notation to make it more difficult to make mistakes

can just put these anywhere in the text.

The Crystal Exchange will validate your document, it will try to show errors e.g. contradictions, wrongly used codes, ...

## how to specify the offer

- write a markdown page
- specify all required tags just by ```$tag:$...``` anywhere on the page
- define the price with the price definition codes
- can specify specific product code

## technical aide

- you can include other docs, this allows you to avoid duplicated content
- e.g. can create 4 pages including the same photos, product description, ...
- on each page there can be other price, ... or other tags, or ...
- everything can be mixed & matched

## processing & matching engine

In the near future there will be a very simple matching language which people can use to define custom rules, this is incredibly powerful.

e.g.

```python
if customer in location.europe:
	discount = 10%
if customer in location.32:
	discount = discount * (1-10%) #lower the discount with 10%
if customer == id.kristof:
	discount = 100%
if customer in circle.acircle:
	price = 10 USD
if customer in location.europe and product.weight>1kg:
	error "cannot ship to you location, too heavy"
if customer in location.heaven:
	print "thank you, you don't need anything, you are already in heaven"
	nomatch
```

how does this work, first based on the tags the buyer gets matched by the provider then the matching rules are applied, if issues then will be reported back or can be silent and just not match.


