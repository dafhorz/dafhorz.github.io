---
layout: post
title:  "Marketing Campaign Results"
date:   2023-02-12 00:43:33 -0600
categories: Marketing
tags:
  - ETL
  - Tableau
  - Dashboard
  - SQL
  - Python
  - Pandas
permalink: /MarketingCampaignResults
image: 
  path: /assets/images/retail-store.jpg
  thumbnail: /assets/images/retail-store-400x200.jpg
  caption: "Photo from [Pexels](https://www.pexels.com)"
---


'Maven Analytics' uploaded a Marketing Campaign dataset (2,240 customers) which includes customers profiles, product preferences, campaign successes (or failures) and performance. Following their recommendations as a guideline, I did a whole ETL pipeline process and presented it in a Tableau dashboard (which can be seen [right here]). 

I extracted the data from [MarketingDataSet], cleaned and transformed the dataset using Pandas, exported the processed file(as CSV) and loaded the set to MySQL (pymsql). The whole explanation can be seen in the Notebook stored right here: [MarketingNotebook].

[MarketingDataSet]: https://maven-datasets.s3.amazonaws.com/Marketing+Campaigns/Marketing+Data.zip
[right here]: https://public.tableau.com/app/profile/manuel.romo.de.vivar/viz/MarketingCampaignResuts/Dashboard1
[MarketingNotebook]: https://github.com/dafhorz/MarketingCampaignResults
