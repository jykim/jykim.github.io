---
layout: post
title:  "Lessons from Netflix Recommender System"
date:   2016-02-04 18:17:43 -0800
categories: blog
---

Recently, Netflix published [a journal article](http://dl.acm.org/citation.cfm?id=2869770.2843948) about their recommender system, focusing on evaluation and its impact of business in general. While I mostly work on evaluation for search, evaluation of recommendation system is a closely-related problem. (In Netflix, search powers 20% of video views, the rest is by recommendation) Here I plan to provide a quick summary focusing on what we can learn from this.

They cite the increase and video collection utilization as main value of recommendation system. In the chart below they show how personalized recommendation increase effect collection size and engagement rate, compared to just showing popular titles.

![](/images/020516_0050_Lessonsfrom1.png)

They also compare offline (judge-based) and online (user-based) evaluation. Partly due to the personalized nature of the recommendation, they found that it is hard for a judge to make reliable assessment of which list is better (examples below), thus mostly rely on online metrics.

![](/images/020516_0050_Lessonsfrom2.png)

They use a variety of online metrics for measuring user retention and engagement, and they report high correlation between retention and satisfaction metrics. Retention metrics are directly linked to their bottom line, so that's of foremost importance. However, they want both retention and satisfaction metrics to move when making ship decisions, to avoid false positives.

It's also interesting that they run online tests for much longer periods (2~6 months) than what's known for search evaluation (1~2 weeks). This is due to their emphasis on retention metrics. Since this long turnaround time can slow down their iteration, they use various offline experimentation technique. (I [published a paper](http://dl.acm.org/citation.cfm?id=2685311) about offline prediction of online experiments last year)

![](/images/020516_0050_Lessonsfrom3.png)

This Netflix article shows that the problems faced by online service companies are not unlike from each other. There was also [an article about Facebook's experimentation of feed ranking](http://www.slate.com/articles/technology/cover_story/2016/01/how_facebook_s_news_feed_algorithm_works.single.html), where they talked about how they combine online and offline experimentation for continually improve the quality of the news feed. The main takeaway in both cases seems to use multiple complementary metrics for decision making to measure elusive notion of user satisfaction.
