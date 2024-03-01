---
tags:
  - datapods
  - publish
Related: 
slug: 
title: "The GDPR Files: What Mark Zuckerberg Knows About You"
path: articles
---
![markzuck.jpeg](/assets/markzuck-f0a30751879156b687a0c63d17fb77ec.jpeg)

The European Union's General Data Protection Regulation ("GDPR") is the most comprehensive privacy regulation in the world. If you're here, you probably already know that it allows you to request a copy of all the data a company holds about you. But have you ever tried it yourself? If you want to, here are some of the surprising things that you might find. 

For the sake of simplicity, this article is divided into three sections, each dealing with one of the three levels of data collection. The deeper we go along this 'data iceberg', the less transparent become the means of data collection and the purposes for which the resulting information is used.

![dataiceberg.png](/assets/dataiceberg-faee8c7bd1384d27f6b2ac1cf307d84f.png)

# Level 1: Volunteered Data

The tip of the iceberg: Facebook and Google know everything you explicitly tell them about yourself. This usually includes at least your name, email address and date of birth. However, some users may choose to volunteer a whole range of additional information that goes well beyond what is required by the online platforms to provide their services: Addresses, Professional Details or even Relationship Status are all fairly common on platforms like LinkedIn or Facebook. 

This type of information is usually featured on your profile or you can view and edit it in the site settings. While more sensitive details like your date of birth or address often remain private by default, a lot of the information provided could be public for everyone to see, depending on your privacy settings. 

# Level 2: Collected Data

It should come as no surprise that internet platforms store and use the data you volunteer to them. However, things get a lot less transparent when it comes to the data they collect about you from your activities and app usage. Everything you look up, click or watch is stored. Most navigation services also store your entire location history. My co-founder Jakob recently looked at his Google Maps data and found that the service had recorded about 38.8 million lines of GPS data. If you were to print that out, it would make more than 1,000 books as thick as the Bible.

But that's not all: Did you know that many services track everything you do on their website, even if you don't click on anything? The resulting data is often used to optimise a site's usability or to find out what type of content you look at the longest. This is what it looks like when we enable session replays in our website analytics tool (PostHog). You're watching Jakob trying to subscribe to our newsletter for the second time because it's just so damn good. Look at him go!

![posthog_recordings.gif](/assets/posthog_recordings-05146ec3ceb4b6cc576e5ab9011be26a.gif)

Some analytics tools will also save the information you type into a text field even if you don't press a button to submit it. So be careful about entering passwords or sensitive information in fields that aren't explicitly marked as password fields, or on a site you don't trust.

> Disclaimer: Datapods is not interested in your personal information. We try to store as little data about you as possible. The Datapods app uses high-end encryption and decentralised key management to prevent unauthorised access to your data, including by Datapods itself. This way you stay in full control of who knows what. 

Businesses use this type of information to improve their services, figure out what you like, and serve you personalized ads. However, for users it is usually not as easy to access. While you can often view a summary of certain collected information such as reactions, comments, or your search history, other information remains hidden. This is where the EU and the General Data Protection Regulation (GDPR) come in. The GDPR allows you to request a copy of your data. That is, every piece of information that can be traced back to you. This includes most types of collected data.

The process of requesting this information can be a little more elaborate and take several days (under the GDPR, companies have to comply within 30 days). The resulting data has to be provided in a machine-readable format, like a JSON file. While this would likely make for a real page-turner, if your name is C-3PO, humans tend to have a hard time trying to enjoy it. That doesn't mean you're going to be looking at ones and zeros, but when you're sifting through 38.8 million lines of raw GPS coordinates, you might as well be.

However, let's say you already requested a copy of your data from a service like Facebook or Google. Here are some of the things that might still be interesting to check out: For example, Facebook keeps track of your most recent location (`last_known_location.json`), purchases made through their app (`payment_history.html`), and the ads you've looked at. 

Ever wondered why you sometimes start seeing ads on Facebook for items you looked at on a completely different site? Under `advertisers_using_your_information.html`, Facebook lists all the companies that use your personal information to target ads to you. These companies already have information about you in so-called "audience lists", which they have collected or purchased themselves, for example, whether you looked at an item on their website. Facebook then combines that information with its own data to make ads even more hyper-personalised. For me, this list is about 120 companies long and includes various data brokers.

But there's more: I recently requested a copy of my data from Payback, the Master Card owned retail bonus program. I got the entire record of my real-life in-store purchases that I made using my royalty card plus a detailed history of whenever I was close to one of their partner stores. Or are you trying to remember what song you were listening to on May 9th 2022 at 6:28 am? Don't worry, Spotify's got you covered with a complete streaming history. 

```json
{
	"endTime" : "2022-05-09 06:28",
	"artistName" : "alt-J",
	"trackName" : "Breezeblocks",
	"msPlayed" : 1340
},
{
	"endTime" : "2022-05-09 06:28",
	"artistName" : "Monolink",
	"trackName" : "Return to Oz - ARTBAT Remix",
	"msPlayed" : 260493
},
```

The few examples provided above really only scratch the surface of the collected data that could be out there about you. The amount of usage data that companies collect is enormous. Just the folder of my information from selected Google services, contains 3.7 GBs worth of raw data stored in more than 5,000 individual files. 

However, just knowing that you ate an entire box of 20 Chicken McNuggets on a wednesday night at 1:35 am isn't going to make Mark Zuckerberg [$270 of annual average revenue per user](https://www.datapods.app/blogs/what-your-data-is-actually-worth). Instead, companies use this information to make inferences about you, which are far more useful to them. This brings us to the very deepest part of the data iceberg, where the water is murky and sunlight rarely reaches...

# Level 3: Inferred Data

This is where it gets really interesting. Data storage isn't free, and tech companies wouldn't be collecting gigabytes of information about you if they didn't think it would be useful at some point. The truth is that they need these vast amounts of data for analysis. The results can be used to categorize you into groups for targeted advertising or improved content suggestions. 

In addition to your detailed location history, google also uses the speed at which you're traveling and a variety of other factors to figure out what method of transport you're using. It also makes guesses about the route and timing of your daily commute. 

The data provided by Meta under the GDPR also contains a list of your inferred interests for content (e.g., `your_topics.json` for instagram) and advertising (e.g., `ads_interests.html` for Facebook). Instagram thinks I'm into "Food", "Travel Destinations" and "Interior Design", which is pretty accurate. However, I was also marked down for the category "Bugs & Worms", a hobby I have yet to discover. 

```json
{
	"title": "",
	"media_map_data": {
	},
	"string_map_data": {
		"Name": {
			"href": "",
			"value": "Bugs & Worms",
			"timestamp": 0
		}
	}
},
```

If a user is into US-Politics, Facebook might even make assumptions about their political affiliation, which also show up here. Advertisers can use this information to show politically targeted content. 

However, if you're launching a political campaign to convince people to vote for you, the categories provided by Facebook might be a bit too blunt. But don't worry, there's a solution! Remember the "audience lists" from before, that allowed firms to combine their own data with Facebook's? Back in 2018 Facebook got in trouble for allowing a political consulting firm called "Cambridge Analytica" to do exactly that. 

CA used users' psychological profiles they previously obtained through a survey and combined it with data on their Facebook friends to target swing voters and show them content that would discredit their client's opponent. While the overall effectiveness of the campaign remains uncertain, this illustrates one of the many ways, that companies and political actors can combine the previously mentioned tools with powerful data analysis to their advantage. 

But that's not all: When companies aren't using their 1,000 bibles worth of your personal information to influence your voting behavior or decide whether you're more of a bug or a worm person, they can get pretty creative with it. 

For example, credit reference agencies (like the SCHUFA in Germany) will use the personal data they obtain from financial institutions to calculate your credit score, which banks then purchase to determine how likely you are to default on a loan. Since your credit score is obviously tied to you as a person, you are also entitled to request it for free under the GDPR (even though the agencies would like you to believe otherwise). 

According to several sources, the dating platform Tinder used to calculate something similar to a credit score, just that they were rating their users' attractiveness in order to match them up with similarly attractive people. However, the company claims that they abandoned that materic a couple of years ago in favor of a more "dynamic system", so you won't be able to see it by issuing a GDPR request.

# Take Control over Your Data

The GDPR is an incredibly powerful tool when it comes to giving you control over the vast amounts of data collected by Big Tech. The ability to access, understand and decide what happens to this data is a huge step forward in protecting privacy and ensuring that individuals can make informed decisions about their digital footprint.

However, the process of accessing or deleting your data can be so daunting that most people will choose not to go through it at all. And when you do get a copy of your data, the information companies provide is usually in machine-readable formats like JSON, which, let's face it, isn't exactly user-friendly for most of us. This is where Datapods comes in.

We've built Datapods to be your digital ally, giving you the power to view, manage and even share your data in a way that's secure and straightforward. Think of it as decluttering your digital life and putting you back in the driver's seat. Datapods are all about making the complex world of data easier to use and putting control back where it belongs - with you.


