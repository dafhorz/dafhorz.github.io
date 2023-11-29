---
layout: post
title:  "Data Wrangling Challenge in Excel: Salary Survey 2021"
date:   2023-02-12 00:33:33 -0600
categories: Wrangling
tags:
  - Excel
  - Wrangling
  - Cleaning
permalink: /ExcelWranglingChallenge
image: 
  path: /assets/images/excel.jpg
  thumbnail: /assets/images/excel-400x200.jpg
---


'Maven Analytics' uploaded a Marketing Campaign dataset (2,240 customers) which includes customers profiles, product preferences, campaign successes (or failures) and performance. Following their recommendations as a guideline, I did a whole ETL pipeline process and presented it in a Tableau dashboard (which can be seen [right here]). 

I extracted the data from [MarketingDataSet], cleaned and transformed the dataset using Pandas, exported the processed file(as CSV) and loaded the set to MySQL (pymsql). The whole explanation can be seen in the Notebook stored right here: [MarketingNotebook].

[MarketingDataSet]: https://maven-datasets.s3.amazonaws.com/Marketing+Campaigns/Marketing+Data.zip
[right here]: https://public.tableau.com/app/profile/manuel.romo.de.vivar/viz/MarketingCampaignResuts/Dashboard1
[MarketingNotebook]: https://github.com/dafhorz/MarketingCampaignResults