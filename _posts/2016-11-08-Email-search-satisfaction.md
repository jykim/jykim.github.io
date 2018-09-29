---
layout: post
title:  "Measuring Success and Satisfaction for Email Search (SIGIR'17)"
date:   2016-02-04 18:17:43 -0800
categories: blog
---
Email has been a dominant form of communication for many years,
and email search is an important problem. In contrast to other
search setting, such as web search, there have been few studies
of user behavior and models of email search success. Research in
email search is challenging for many reasons including the personal
and private nature of the collection. third party judges can not
look at email search queries or email message content requiring
new modeling techniques.

In this study, we built an opt-in client application which monitors
a user’s email search activity and then pops up an in-situ survey
when a search session is finished. We then merged the survey data
with server-side behavioral logs. this approach allows us to study
the relationship between session-level outcome and user behavior,
and then build a model to predict success for email search based
on behavioral interaction patterns.

Our results show that generative models (MarkovChain) of success
can predict the session-level success of email search better
than baseline heuristics and discriminative models (RandomForest).
The success model makes use of email-specific log activities such
as reply, forward and move, as well as generic signals such as click
with long dwell time. The learned model is highly interpretable,
and reusable in that it can be applied to unlabeled interaction logs
in the future.

[Link to the Paper](https://rawgit.com/jykim/jykim.github.io/master/files/understanding-modeling-success-email-search.pdf)