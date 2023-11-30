---
layout: post
title:  "Insights for an Internet Service Provider"
date:   2023-09-11 00:43:33 -0600
categories: Sales Telecom
tags:
  - EDA
  - Excel
  - Dashboard
  - Automation
permalink: /Proper_Internet_Insights
image: 
  path: /assets/images/internet-provider.jpg
  thumbnail: /assets/images/internet-provider-400x200.jpg
---

## Summary
Utilized Excel for comprehensive data analysis and error rectification in an Internet Service Provider's billing system, resulting in substantial cost savings. Identified strategic insights, which were presented through a user-friendly dashboard, and proposed proactive error strategies to enhance overall operational efficiency.

## Achievements
**Cost savings**
: Identified several errors in billing data, resulting in an annual savings of 73,304 Quetzales or 9.5k USD (assuming a linear behaviour under a constant workload).

**Insights**
: Popular sectors, profitable clients, key services, and employee productivity, leading to strategic recommendations for business enhancement.

**Proactive Error Strategies**
:  Introduced proactive error strategies by analyzing date patterns and incomplete records, addressing potential issues.

# **Important**
**Due to confidenciality of the enterprise and data privacy, this project is not available to download. So I'll limit myself to share very few details.**

## Procedure

### Objective
> The provided report contains an error in the sales breakdown, as it does not align with the total billed amount. Additionally, the client requests additional pertinent information regarding their business.

### Exploration
Through an exploration analysis, *canceled service* seemed to be managed as an *active service*. Besides that, the system had registered services that are not available anymore, which were supposed to be merged with a new service. Both easily solved by IF and SUMIFS statements.

### Wrangling
A very subtle change in the format of the product catalogue helps to automatize and prevent errors.
<figure class="align-center">
  <a href="#"><img src="{{ site.url }}{{ site.baseurl }}/assets/images/Proper_Internet_Insights/catalogo-antes.JPG" alt=""></a>
  <figcaption>Product catalogue before.</figcaption>
</figure>  

<figure class="align-center">
  <a href="#"><img src="{{ site.url }}{{ site.baseurl }}/assets/images/Proper_Internet_Insights/catalogo-despues.JPG" alt=""></a>
  <figcaption>Product catalogue after.</figcaption>
</figure> 



Now is easy to use *XLOOKUP* and conditional formatting to fix the sales report. Here's a summary: 
<figure class="align-center">
  <a href="#"><img src="{{ site.url }}{{ site.baseurl }}/assets/images/Proper_Internet_Insights/facturacion-antes.JPG" alt=""></a>
  <figcaption>Billing summary before.</figcaption>
</figure>  <figure class="align-center">
  <a href="#"><img src="{{ site.url }}{{ site.baseurl }}/assets/images/Proper_Internet_Insights/facturacion-despues.JPG" alt=""></a>
  <figcaption>Billing summary after.</figcaption>
</figure> 

### Insights
A summary on my insights. Due to data privacy, I'm substituting text and values with **xxxxx**.
> Cable service proves to be **xxx** times more profitable than internet service, with service **x** being the most popular among clients, constituting over **xx**% of contracts. Notably, all clients, except for **xx**, have opted for service **x**, totaling **xx** contracts.
> 
> While the income by invoice date currently lacks significance due to data limited to December, it could become more informative with additional recent records.
> 
> The presence of **xx** incomplete records is unfortunate. It's advisable to investigate whether this stems from a platform bug or a client-side incident. Notably, all incomplete records have unique Series values, making completion through analysis unfeasible.
> 
> The "Most Popular Sectors" and "Most Profitable Customers" charts are affected by noise from these records but can be filtered for clarity.
> 
> The absence of user profiles hinders the analysis of preferences, demographics, and economic situations, limiting our ability to project future trends. Requesting this information from the client is recommended if possible.
> 
> Lastly, **xxxxxxxx**'s productivity is notably higher compared to colleagues, wich raises suspicion. A review is recommended to ensure it's not an error or a pre-fill defaulting to this user.