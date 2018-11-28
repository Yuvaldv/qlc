---
title: Data Validation
weight: 4
pre: ""
---

While it may seem trivial that the integrity of our dataset is flawless, and that each datapoint is reliable in it's naming convention along with its flow across different platforms. most times this is hardly the case.

Thus, it's necessary for us, as analytics specialists, both to define the naming conventions of our datasets as well as run QA tests on the analytics setup created by the development team so we don't wake up 3 months into the data collection process and realize we severely misinterpreted our data the entire time.

## Data Flow
While many times data flow will be fairly simple, going straight from our app or website into our analytics platform, in some instances things won't be so simple such as measuring how many users encountering our landing page installed our mobile app. in this instance our user's ID parameters need to transfer from our landing page to the AppStore, then into our app and to our analytics platform from there, thus a single user creates several data points that cross 4 different platforms in order for us to read it.

Let's take a look at several different methods for data transfer, and how to utilize them.

### Websites & Web-apps

#### URL Parameters

These are parameters attached to a URL in Address link via the `?` symbol. These have varied uses, from keeping search queries, user data, arrival sources to our URL, and more.

```
https://www.google.co.il/search?q=search+for+common+ground&oq=search+for+common+ground&aqs=chrome..69i57j0l5.4243j0j7&sourceid=chrome&ie=UTF-8
```
In this example we see that:

`?q=..` is the user's search query,

`&sourceid=..` is where the query was entered. since it's a added to another parameter it uses the '&' symbol instead of `?`.

`&ie=..` is the encoding used on the users browser.

The rest are google proprietary information, and though it's completely unnecessary, [here's where](https://moz.com/blog/the-ultimate-guide-to-the-google-search-parameters) you can read more about them.

Here's where you can [learn more](https://en.wikipedia.org/wiki/Query_string) about URL parameters.

#### UTM Codes
UTM codes are standard URL parameters used for analytics purposes. These codes provide us with a tool to measure the performance of our inbound links and track the amount of traffic coming from each of our publishing platforms, search results and ad-placements.

Using UTM codes, which are read as a standard by all analytics platforms e.g KissMetrics, Mixpanel, Heap and of course Google Analytics, you can track broad sets of data such as how much traffic your receiving from each platform (google search, google adwords, facebook, twitter, etc.), You can also track highly specific data such as how much traffic you're getting from the Call-to-Action on your Facebook page against each post on the same page.

|   UTM Parameter   | Purpose | Example | Required? |
| ---- | ---- | ---- | ---- |
| source | Indicates which domain sent the traffic our way | `utm_source=Facebook` | V |
| medium | Indicates which type of link was used, cost-per-click, post, email, etc. | `utm_medium=PageCTA` | V |
| campaign | Indicates the name of our campaign and has varied uses. | `utm_campagin=spring_sale` | V |
| term | Identifies search terms used by the user | `utm_term=running+shoes+sale` | X |
| content | identifies the specific component clicked by the user that referred them to our website | `utm_content=logoclick` `utm_content=textclick` `utm_content=titleclick` | X |
| id | the campaign id is used to attribute all other parameters like `campaign` or `source` in accordance with the `id` | `utm_id=google_CPC_july` | X |

When defining and implementing you UTM parameters in posts, content, page components etc. keep the following in mind:
1. Do not use them for internal links on your own website. Following user interactions using UTM codes is a futile effort and there are far more advanced techniques for this attempt. The use of UTM codes, as we said, is following outside traffic sources leading to our website.

2. Make sure to properly mark and segment paid traffic using the `utm_medium` parameter e.g CPC or CPM, from organic traffic such as posts or articles. Not doing so will weaken your position to establish return-on-investment from paid sources and will highly damage your competence to derive actionable insights from your analytics.
3. Not documenting your UTM code placement could be a fatal error leading to severe ambiguity later on. Do make sure to create a shareable sheet and tracking your UTM Codes. Use [this template](/qlc/assets/DA/UTM_Codes.xlsx)
4. the `utm_campaign` parameter is highly versatile and can be used a great number of ways such as tracking campaigns for:
   1. Seasonal promotions
   2. A specific product line such as `shoes`, `jackets`, `t-shirts`
   3. A specific brand such as `nike`, `adidas`, etc.
   4.  A targeted buyer persona such as `programmer-Tim`, `projectManager-Kevin` .
   5. A specific outcome from the call-to-action such as `hot-lead`,`cold-lead `,`trial`, `beta-request`, `add-to-cart`

   These sorts of naming conventions allow you to measure you're campaign results and compare them over time via these segments, so useful.

In order to avoid the complexity of writing the the full URL including all UTM codes you may want to use [Google URL Builder](https://support.google.com/analytics/answer/1033867?hl=en). And so we don't present the user with long and suscpicious links, we'll shorten our URLs using [bit.ly](https://bitly.com/) or similiar.

[UTM.io](https://web.utm.io/) is also a great tool for working with UTMs. It integrates URL building, shortening & tracking, so convenient.

#### JavaScript Integrations

Analytics platforms such as [Heap](http://www.heapanalytics.com), [Mixpanel](http://www.mixpanel.com), [CrazyEgg](http://www.crazyegg.com), [HotJar](http://www.hotjar.com) in general are integrated into websites & web-apps via inserting a *JavaScript tracking snippet* into our page's code. Though it's literally as simple as copy-pasting, it must be attached to each and every one of our webpages.

[Here's and example](https://docs.heapanalytics.com/docs/installation#section-web) from HeapAnalytics on how to insert a snippet into your webpages for one of many analytics platforms. Don't forget to change `YOUR_APP_ID` parameter to your account details.

When using multiple platforms it may seem like you need to insert multiple snippets, one per platform, into your `</head>`, this arises concerns towards a slowdown page-loading-time. for this we'll use a Tag Manager such as [GTM](https://www.google.com/analytics/tag-manager/), which allows for us to integrate a single, permanent snippet into our webpages and use a the Tag Manager to add, remove and manage integrations of various analytics platforms that will receive data via that same snippet.

##### Event tracking
While it may be tempting to track all events on your website without discriminations it important to remember that the product of good analytics isn't a wide collection of data-sets, but the quick arrival at actionable insights from those data sets.
To the latter, auto-tracking events are most times counterproductive due to computer-generated naming conventions and lack of relation to other data sets used to form funnels.

Thus it is best to define the events you'll be tracking and the questions or hypotheses these events will be tied to before any data has been collected.

##### Custom Properties
While each analytics platform has a [standard set of properties](https://help.mixpanel.com/hc/en-us/articles/115004613766-Default-Properties-Collected-by-Mixpanel) which tell us more about the user, such as location, timestamp, operating system, browser, etc. We may require further details to arrive at meaningful conclusions. Thus after setting our events we should want to create custom events to have some more context for each type of user.

## Data Coherence

When initially defining our dataset, prior to the data collection, It’s important to name each of our parameters as well as their values in a manner which we’ll be able to immediately recognize when we approach the data analysis. Naming a parameter triggered on the first app onboarding screen “FinishedOnboarding”, for instance, would be a bad idea, because for the user the onboarding just started.

## Significance of Results

### Sample Size vs. Effect Size

Allow me to quote Phillip Porter of MecLabs for a second, as he clears everything up pretty neatly:

>“Significance is based on sample size and effect size. The larger the sample you have, the smaller effect size you can find to be significant. The larger the effect size present, the smaller sample size you need to find significance. Larger sample sizes are generally better, however any difference, no matter how small, can be found to be significant with a large enough sample size.”

Whereas sample size refers to the overall amount of people participating in the A/B test and effect size refers to the 𝚫delta between the two groups.

$ EffectSize = \frac{Mean A - Mean B}{StandardDeviation} $

As a general rule we’ll be needing a sample size of a couple of thousand users per test, at the least. We’ll also need to record the test results through time and not as any one final measurement. Like anything though, it’s all a matter of finding the right measure and relying on good intuition, your own as well as that of your team.

Evan Miller’s A/B test [calculator](http://www.evanmiller.org/ab-testing/sample-size.html) is my personal favorite and an industry standard,

Here’s another [set of calculators](http://www.sample-size.net/), not as popular but useful non-the-less in helping you with deciding on proper sample sizes, effect sizes and confidence levels. There are many more out there just a google search away.
