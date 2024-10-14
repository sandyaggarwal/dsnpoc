---
title: RSS Feeds
slug: ZaCG-rss-feeds
createdAt: Tue Oct 24 2023 10:20:34 GMT+0000 (Coordinated Universal Time)
updatedAt: Tue Oct 24 2023 10:26:15 GMT+0000 (Coordinated Universal Time)
---

# RSS news feeds

1. Locate the RSS feed source (url)
2. Fetch feed content on your website
3. Configure the mapping of feed fields if necessary
4. \[Optional] Build page for displaying article details
5. Styling

### **1. Locate the RSS Feed**

You need to find URL at which RSS feed is available. You may either get it from a customer or find it on your own (if it exists). Try searching web, including the customer page name and 'rss feed url'.
You are looking of an URL that renders an XML structure of \<tags> containing feed details and details of several articles

EXAMPLE: When looking for The Guardian's RSS feed in web browser, you'll likely find this help page:[ https://www.theguardian.com/help/feeds](https://www.theguardian.com/help/feeds). It describes how to use various thematic feeds. Let's use <http://www.theguardian.com/world/rss>.

### **2. Fetch feed content on your website**

In order to use this feed you need to load it somehow on your DSN Website. You can do that by adding **RSS > Feed - \*** component and pasting feed url there. Now, when this page is opened, latest feed is fetched and cached locally.

EXAMPLE: Open your web project's home screen and add **RSS > Feed - List **component. Then, paste feed URL. And run project. Don't worry about fixing the styling at this point.

![](https://2470783510-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MMLrO7TweNFMn8PgeVh%2Fuploads%2FL8Ce8qSpQKXAxxJzVFx5%2Fimage.png?alt=media\&token=56badc7f-811b-4b99-873b-32ede8995c8c)

### **3. Configure mapping of feed fields**

Feed components are designed to work with The Guardian by default. This may not be the case for all feeds. Some of them may have a different structure, or store some information in different places.&#x20;

If you notice any information, like title, image, date, etc. missing from your articles, open the component used to fetch the feed and click the button under Content Mapping field. This will display a mapping dialog.&#x20;

![](https://2470783510-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MMLrO7TweNFMn8PgeVh%2Fuploads%2Ffq22d69dmUSTTP2B5NM1%2Fimage.png?alt=media\&token=4d53d885-c100-4f5e-a4b8-f4b518601bc7)

Getting this part done requires some technical knowledge, so feel free to reach out to DSN team for help. In general, first column is a \<tag> name that searched your value, second - allows to select which property should you value be used as. Keep Array column is used to state if there is more than one of specified tags in a single article. Last column - Selector - is used to extract values that are not specified within the tag (\<tag>value\</tag>) but rather as tag's attribute (\<tag attr="value">\</tag>). In this case you can reference the attribute with selctor: **.$.attr **and if there is more than one tag of your selection and you selected Keep Array as true, then you can reference particular element with zero-based index as **.0** selector.&#x20;

EXAMPLE: Guardian's feed has two images - a thumbnail and a full-scale image. Both urls are provided as \<media\:content url="..."> next to each other, but thumbail is always first, and orignal - second. You can see their configs in the screenshot above.

You need to update the mapping of each component that fetches your feeds.

### **4. \[Optional] Build page for displaying article details**

You can choose to handle article clicks in serval ways, eg. by redirecting to original article or rendering article content on your custom article screen. To do that, you will need just one page that will use **RSS > Article - \* **components to fetch appropriate article's content. Article page creation in itself is quite straightforward. It can look like this:

![](https://2470783510-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MMLrO7TweNFMn8PgeVh%2Fuploads%2FALlSVk9AtwrvOvtiUo15%2Fimage.png?alt=media\&token=e22a16ff-2a0c-4b47-936f-e3fa6872aa37)

- **On click**: "Open in custom screen"
- **Link to**: "Article" (your article template screen)

![](https://2470783510-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MMLrO7TweNFMn8PgeVh%2Fuploads%2FL8Ce8qSpQKXAxxJzVFx5%2Fimage.png?alt=media\&token=56badc7f-811b-4b99-873b-32ede8995c8c)

Now, if you click on an article card on the feed list, you will be redirected to your article screen and **?articleId=1234567** parameter will appear in URL. This parameter is used to decide which article details to load.&#x20;

**NOTE: Article with given articleId needs to exist in your cache (localStorage), so avoid using direct links to article page.**

### **5. Styling**

Once configuration and the whole mechanics is set up, you can use each component's properties to tweak how it behaves and looks. This includes number of items to render, card width, click behavior, layout, alignment or even date and time formatting.

