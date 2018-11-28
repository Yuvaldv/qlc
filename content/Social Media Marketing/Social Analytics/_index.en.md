---
title: Social Analytics
weight: 4
pre: ""
---

Analytics means the collection and analysis of data: organic as well as available market data, in an aspiration of gaining meaningful insights into how we could better our social presence as well as validate those assumptions upon which our current actions are based on. While it’s easy to get lost in all the data available today, once you know what it is you’re looking for, things become much clearer.

## Market Research

Using different analytics solutions for each of our social platforms (available under Tools & Templates), we’ll research what sort of content works best within our market-niche, for each of our main-competitors and best engages our target-audience. We’ll attempt to gain insights into those specific days-of-the-week, times-of-day, titles, keywords, media types, and other content segments which worked best for them in terms of engagements, and in terms of conversions, separately.

## Objectives & Key Results (OKRs)

Objectives and Key Results (OKRs) are a set of objectives accompanied by metrics, often called Key Performance Indicators (KPIs) to measure our empirical success, e.g:

Reach & Impressions - Refers to the number of users exposed to our social content.

Engagement - Refers to how users interact with our content on each social platform

Behaviour & Conversion Rate -Refers to how users engage with our brand website via social referrals.

        * % referral traffic from the social platform vs. Overall Traffic

        * % referral traffic from the social platform vs. Social Traffic

        * Platform Referral Traffic Bounce Rate

        * Platform Referral Traffic Session Duration

        * Platform Referral Traffic Pages per session

        * Platform Referral Traffic Time on Page

        * Platform Referral Traffic Comments

    * These KPIs will be tracked on our own domain via GA, Mixpanel, etc.
      For more info please refer to our Data Analytics curriculum.

It’s imperative to derive your SMM objectives from your primary Business Objectives so as to avoid focusing on vanity metrics which won’t really get you or your business anywhere, leaving you measuring ‘how many holes it takes to fill Albert Hall’ i.e have a lot of metrics on things of no real consequence.


## Effectively tracking our Posts via UTM Codes

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

## Compound KPIs

Second level KPIs make use of our baseline KPIs such as post likes, followers, comments, etc. and looks to see how they measure up from the perspective of time, audience, or content allowing us for a more comprehensive view of how our strategy and execution is working out.

### Growth

Our growth rate indicates how our KPI is measuring up in relation to past results per the same KPI.

Specific growth and Average (mean) growth may be calculated via these two simple formulas

$specificGrowth = \frac{present - past}{past}$
Calculates growth between two timestamps

$avgGrowth = (\frac{recentTime}{firstTime})^\frac{1}{n} -1 $

Calculates average growth between *n* timestamps

Here’s a [template growth sheet](/qlc/assets/smm/GrowthCalc.xlsx) you may copy and insert real data into.

### Rate

Our rate indicates how our KPIs performance is measuring up in relation to the audience available to it.

If for instance we got an average of 20 post likes per day, a month ago, where our entire page followers were 200, and today we have an average of 40 post likes per day with a following of 1200 users, it’s safe to say our user engagement is on the decline.

Rate is simply calculated as such:
$\frac{metric}{audience}$

### Average

Simply put, our average takes our results and compares it to the deliverables we’ve manufactured for a specific timeframe e.g June 01 - June 30
$\frac{metricSum}{numberOfPosts}$

### Top

Our top performing posts are crucial to our understanding of our audience as well as for inspiration for future work.

## Social Media Optimization (SMO)

After we’ve done enough market research to feel comfortable posting our own content savvily we’ll begin measuring that content, to see what works best for us i.e optimize our social media posts and presence*. We’ll also assign specific time-frames, a week or two, for trying out different tactics we think might work, 1-2 tactics at a time, measuring their relative success via our OKRs to other tactics and our current KPI baseline, thus validating or disproving their hypothetical success for our specific brand and audience.

For each optimization cycle we’ll build or adjust our social posting schedule which could be either wholistic or segmented per platform

![image alt text](/qlc/assets/smm/image_7.png)

## Goal

Once we’ve got a headstart on our social media content and optimization, we’ll also try to understand how we measure up to the competition, mainly in terms of *growth rate* which can be calculated with two simple formulas (see Compound KPIs chapter)

So, to sum it all up, we’re looking to:

* Identify competitor success in terms of engagements

* Identify competitor success in terms of conversions

* Identify our own success in terms of engagements

* Identify our own success in terms of conversions

* Identify us and the competitor market in terms of *growth rate*

**All so we can repeat successful patterns for optimal results.**

## Platform overview

Here are links to SimilarWebs current reports on each of the social platforms we’ll be dealing with:

[Facebook](https://www.similarweb.com/website/facebook.com)    - Needs no introduction

[Twitter](https://www.similarweb.com/website/twitter.com)        - Needs no introduction

[Instagram ](https://www.similarweb.com/website/Instagram.com)    - Facebook’s own contextual photo and video sharing platform.

---------------------------------------

[Reddit](https://www.similarweb.com/website/reddit.com)		- A compound social community.

[Snapchat](https://www.snapchat.com/)    - ‘The fastest way to share a moment!’ apparently.

[Pinterest](https://www.similarweb.com/website/pinterest.com)     - The hobbyist's idea discovery platform.

[Tumblr](https://www.similarweb.com/website/tumblr.com)        - Yahoo’s own social platform used to target 13-25 y/o, now prides itself in rich

   media integrations.

[LinkedIn](https://www.similarweb.com/website/linkedin.com)    - Microsoft’s own social platform aimed at business professionals.

[Twitch     ](https://www.similarweb.com/website/twitch.tv)    - Amazon’s own social video platform aimed at gamers.

Take notice that these reports do not include mobile-app users, only web-visits.

Here’s a more comparative view of the social landscape in [SmartInsights 2017 Social Report](http://www.smartinsights.com/social-media-marketing/social-media-strategy/new-global-social-media-research/), it may be long but if you persevere you get extra-special bonuses such as platform segmentation by demographics and countries (each and every one them 😆).
