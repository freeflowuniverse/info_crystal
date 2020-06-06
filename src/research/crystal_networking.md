# Crystal Networking

Networking is a basic requirement in our modern life, its the fabric of life, through our friends & business contacts we find work, business, love, ...

Today many people even make money out of networking and also this we need to be able to reward.

## Circle Based

- Every person is in many circles.
- Each person can create circles and tag people in it.

Each person has following default circles

- friends
- business
	- generic business relation, without brand
	- intentsity specifies how strong the relation ship is, 10 is most
- organization:$brandname
- country:$countrynr
- region:... (see tags)

I can as a person create as many circles as I want, I can create circles with custom names. Circles can have other circles inside.


## intensity nr's

Every person I put in a circle I can give an intensity nr, if not specified then its a 7.

- The intensity nr's are private and are never revealed !!!
- They are needed to give weight to our relationship with the person in the circle.

### Some examples:

- 'mylove' circle, my intensity nr defines how close I am to true love
- 'organization:threefold', my contact mr X is in it as level 9, which means we are closely connected and find it very easy to trust each other/ do business.
- 'business', my contact mr Y is 6 in business means, is someone I know but not that close in my business network.


## contact making

If I need to find someone I will ask my friends for info/help.
I do this by sending a message to the specified circles where I am looking for help.

## acceptance matrix

To help me do efficient networking I can specify for which circles I accept networking requests and from which intensity level. 

This can be expressed in a acceptance matrix.


```
- friends:+5
- friends:+8auto
- business:+7
- organization:threefold:+9
- organization:myfootballclub:+3
```

Country & Region is not used.

This means anyone i've marked as friend +8 I will help to find a contact and I will automatically forward the request if the destination friend is specified.

## inbox

My inbox is organized per circle and intensity level.

## I need to find something/someone

### if I know the person I am looking for

My CT will send message directly to the person I know, it will arrive in their in box.

#### what if I don't know the person I look for yet.

They I just ask a request to my friends of business contacts starting from a certain intensity.

Example 1: CT send to my friends with intensity +8 that I am looking for the love of my life... If they know someone can they reply with the CT names...
I can then check & ask for specific request.

Example 2: CT send to my business contacts I am looking for a developer with following skills... If they know someone can they reply with the CT names...
I can then check & ask for specific request.


#### I am looking for specific service/product

Each service/product is tagged [see description here](tagging_system.md).
We can use this system to find a service/ product/...

Example: CT can you ask my business contacts ```business:+7``` if they know a ```business``` who does ```service:writing.legal``` in ```location:country:32```

This gives us a very flexible way to get help in finding what we need.

The CT will ask all my business contact of intensity 7 and more if they have business contact which does legal writing, prob means a lawyer in Belgium which has country code 32. My business contacts who have me in their acceptance list will help to find, if ```auto``` used then the request will even be automatic.

This is a powerful way to leverage the power of our network.


