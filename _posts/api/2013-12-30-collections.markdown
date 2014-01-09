---
layout: single
title: Collections
categories: api
resource: collections
---

### Get all collections

	GET /collections

*Description*	

Return the list of all collections in json format. 

*Accepted Parameters*

* collection_id - Return only collections under a specified collection
* format 
	+ "less" - Return less info in order to cut down the response size
	+ "full" - Default value. Return all info under product

*Sample response*

{% highlight json %}
[
	{
		id: "15c",
		type: "collection",
		name: "Beer",
		description: "Beer is an alcoholic beverage produced by the saccharification of starch and fermentation of the resulting sugar",
		images:
			[
				{
					thumb:"http://www.weloveaiden.com/projects/alcoholdelivery/image/cache/data/Product Pictures/PreMix Ready to Drink/Bacardi-Breezer-Lemon-173x173.jpg",
					full:"http://www.weloveaiden.com/projects/alcoholdelivery/image/cache/data/Product Pictures/PreMix Ready to Drink/Bacardi-Breezer-Lemon-173x173.jpg"
				},
				{
					thumb:"http://www.weloveaiden.com/projects/alcoholdelivery/image/cache/data/Product Pictures/PreMix Ready to Drink/Bacardi-Breezer-Lemon-173x173.jpg",
					full:"http://www.weloveaiden.com/projects/alcoholdelivery/image/cache/data/Product Pictures/PreMix Ready to Drink/Bacardi-Breezer-Lemon-173x173.jpg"
				}
			],
		resources:
			[
				{
					id: "259p",
					type: "product",
					name: "Bacardi Breezer Lemon 275ml",
					description: "The best beer in Europe. A must try for everyone"
				},
				{
					id: "25c",
					type: "collection",
					name: "Non-Alcohol Beer",
					description: "Beer with 0% alcohol"
				}
			]
	},
	{
		id: "16c",
		type: "collection",
		name: "Wine",
		description: "Wine is an alcoholic beverage made from fermented grapes or other fruits",
		images:
			[
				{
					thumb:"http://www.weloveaiden.com/projects/alcoholdelivery/image/cache/data/Product Pictures/PreMix Ready to Drink/Bacardi-Breezer-Lemon-173x173.jpg",
					full:"http://www.weloveaiden.com/projects/alcoholdelivery/image/cache/data/Product Pictures/PreMix Ready to Drink/Bacardi-Breezer-Lemon-173x173.jpg"
				},
				{
					thumb:"http://www.weloveaiden.com/projects/alcoholdelivery/image/cache/data/Product Pictures/PreMix Ready to Drink/Bacardi-Breezer-Lemon-173x173.jpg",
					full:"http://www.weloveaiden.com/projects/alcoholdelivery/image/cache/data/Product Pictures/PreMix Ready to Drink/Bacardi-Breezer-Lemon-173x173.jpg"
				}
			],
		resources:
			[
				{
					id: "257p",
					type: "product",
					name: "Bacardi Breezer Lemon 275ml",
					description: "The best wine in Europe. A must try for everyone"
				},
				{
					id: "255p",
					type: "product",
					name: "Bacardi Breezer Orange 275ml",
					description: "Best wine money can buy"
				}
			]
	}	
]
{% endhighlight%}

*Note*

Resouces can contain both products and other collection. Make it flexible for multiple level collection cases.

### Get a collection
	
	GET /collections/:id

*Sample Request*
	
	/collections/10c

*Description*

Return information about the product specified by id

*Sample Response*

{% highlight json %}
{
	id: "16c",
	type: "collection",
	name: "Wine",
	description: "Wine is an alcoholic beverage made from fermented grapes or other fruits",
	images:
		[
			{
				thumb:"http://www.weloveaiden.com/projects/alcoholdelivery/image/cache/data/Product Pictures/PreMix Ready to Drink/Bacardi-Breezer-Lemon-173x173.jpg",
				full:"http://www.weloveaiden.com/projects/alcoholdelivery/image/cache/data/Product Pictures/PreMix Ready to Drink/Bacardi-Breezer-Lemon-173x173.jpg"
			},
			{
				thumb:"http://www.weloveaiden.com/projects/alcoholdelivery/image/cache/data/Product Pictures/PreMix Ready to Drink/Bacardi-Breezer-Lemon-173x173.jpg",
				full:"http://www.weloveaiden.com/projects/alcoholdelivery/image/cache/data/Product Pictures/PreMix Ready to Drink/Bacardi-Breezer-Lemon-173x173.jpg"
			}
		],
	resources:
		[
			{
				id: "257p",
				type: "product",
				name: "Bacardi Breezer Lemon 275ml",
				description: "The best wine in Europe. A must try for everyone"
			},
			{
				id: "255p",
				type: "product",
				name: "Bacardi Breezer Orange 275ml",
				description: "Best wine money can buy"
			}
		]
}	
{% endhighlight %}

