# Testing UX

### Overview
Occasionally, software developers must work on creating some form of user interface. Although UI design isn't a core function of a software developers, knowing how to make a usable and effecient design can help a lot in one's workflow. Understanding where work needs to be allocated design wise can lead to simpler and better features.

User experience can be tested in a [number of ways](https://www.hotjar.com/usability-testing/methods/). It can either be remote or in person, monitored or unmonitored, exploratory or assertive. In the context of Rently, we would like to test the application in its current form to identify potential design flaws or find out whether some features are well implemented design wise.

In this report, we will conduct research on the useability of the [Rently](https://github.com/rently-io) project. More specifically, we will anwser **Are there any design flaws on Rently?** To answer this question, unmonitored remote testing was conducted by simply letting users use the website freely.

Hotjar, a tool made for tracking events (mouse clicks and movements) anonymously, was intergrated into the source code of the website following [these steps](https://help.hotjar.com/hc/en-us/articles/115009336727-How-to-Install-your-Hotjar-Tracking-Code). Hotjar  Data can therefore be collected on a per page basis. A lot can be uncovered throught tracking mouse movements. It can reveal where users' interest is highest and where is it the lowest, it can also reveal user frustration or places in the design where users get stuck. It can also reveal things that were never intended by the developer. 

I asked a random selection of people to use the website freely. With the exception that they use the desktop version of the website, no prerequisite was asked. A total of 13 people tested the website, performing vaiours tasks from simply browsing listings to posting one themselves. Data was collected across the web pages.

#### Home page
This page is the first shown to new users. It's purpose is to educate the user about the service. Although not much textual context is provided, visually, a marquee slider of random listings is displayed above and below a search bar.

Looking at the mouse movements on the home page, people travelled consistantly across the entirety of the focus area and there are clear host spots in some areas. Unlike other pages where the spread is much smaller, a large spread shows that users are [relatively curious](https://cpb-us-w2.wpmucdn.com/voices.uchicago.edu/dist/d/1690/files/2017/01/MouseTracking_Personality_Preprint.pdf):

![](https://i.imgur.com/38AUB0l.jpg)

Around 18% of clicks were made on the "Lease something" button which means the design serves its purpose. Another 10% were made on the "Rently.io" logo (redirecting users to this page). A combined 16% were made on the navigation's "Search" button and on the search input and body's "Search" button. Perhaps shifting the users' attention from the logo by making it less prominant could allocate more clicks to the search options.

> Datasets to all pages present under dataset directory [here](https://github.com/greffgreff/semester-content/tree/main/datasets).

Curiously, 17% of clicks were made on the "meta" banner situated atop the main navigation bar, where the user's location, current date, and language are located. This is a clear design flaw as the meta banner is not intended to be interactive. The fact that almost 11% of those clicks were on the language icon (sourced from the user's browser locale) could suggest that users are interested in a translation. Additional exploratory in person research would be needed to verify this claim.

#### Search page
One big feature about the Rently website is the search page and its search engine. We observe less interactions than the home page, as expected:

![](https://i.imgur.com/xwD7a2o.jpg?1)

One is that the diagram above does not show additional search options extended like so:

![](https://i.imgur.com/EhF5NOC.png)

Superimporsing the two images and looking at the hotspot in the search options area, we can see that there is significant traffic there, 25% of the total traffic specifically. An additional 25% of the interactions occured with the navigation bar and the remaining in various places the majority of which in the results area. 

Given the following, the search page is achieves its goal of enticing users to make searches, though, some design changes could increase interaction to the search options. Automatically expending the search options could increase this.

#### Listing page
Each listing has its own dedicated page loaded dynamically on what is refered as the listing page. The listing page's function is to provide as much incite of the item for rent to the user. Much like the home page, user interaction was made an a large spread:

![](https://i.imgur.com/bMkoB62.jpg)

A hotspot of around 10% is present where, like the search page, an image is missing on the diagram. This reveals that a fullscreen mode for images could be a feature users may be interested in.

10% to 15% of interaction occured around the text of the address just above the map under "Where can I find this" section. This text is not interactive. Users may have expected the address to open a link to google maps directly. 

Finally, around 35% of the interaction occured around the dates in the first section and the description, showing kin interst from the user. Clicking the dates could open a section to visually show the dates on a calendar.

#### Login page
The login page is relatively straightfoward with only the central box with different social providers:

![](https://i.imgur.com/iAbBD5X.jpg)

37% of users interacted with the Google provider. Being the first option, its position is already optimal. 9% of users chose the Twitter as a provider of chose compared to 5% with Facebook. It is best to switch the Twitter providers to the second spot and put Facebook on the thrid spot.

20% of users interacted with the "Back" button redirecting to the home page, once again showing the effectiveness of the design. Wether users are willing to login or not is another matter, though, those that do not wish to login can quickly cycle back to the home page. 

However, much like before, 18% of the interaction occured on the meta navigation bar showing users' great intrest in it. Perhaps those that did not interact with it on the home page noticed it on the login page. Removing the meta navigation bar altogether from this page could draw attention elsewhere.

#### Account page

### Conclusion
Additional exploratory testing needed to validate some claims.

### Works cited

[What is mouse tracking](https://bootcamp.uxdesign.cc/mouse-tracking-what-it-is-and-how-to-use-to-understand-user-behaviour-30180e6da44c)
[Some mouse behavioural patterns](https://www.trymyui.com/blog/2016/10/28/mouse-movement-patterns-and-user-frustration/)
[Mouse movement revealing personality](https://cpb-us-w2.wpmucdn.com/voices.uchicago.edu/dist/d/1690/files/2017/01/MouseTracking_Personality_Preprint.pdf)

Data analysis : https://ictresearchmethods.nl/Data_analytics

Usability test : https://ictresearchmethods.nl/Usability_testing

Observation : https://ictresearchmethods.nl/Observation

UX for IP : https://fhict.instructure.com/courses/12078/pages/ux-for-software-engineers-the-basics?module_item_id=749934

