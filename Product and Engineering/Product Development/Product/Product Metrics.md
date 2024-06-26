---
tags:
  - Product
  - Metrics
---
# Description
# Types
## Predictive and Historic 
Similarly to [[Commercial]] disciplines, the [[Product]] domain also uses [[Leading Indicator|Leading]] and [[Lagging Indicator|Lagging]] indicators for determining the performance of the [[product]]. The [[Product Management]] role  will need to also understand, and potentially monitor, [[Commercial#Types of Metric|Commercial Metrics]] such as [[Return on Investment]] or [[Cost of Delay]] to judge what to act upon, prioritise or otherwise disregard. As the role ultimately has [[Glossary#^Accountability|accountability]] for their [[product]], they will likely also have understanding or input into the [[Pricing Strategy]], even if this is lead by one of the [[Commercial]] team.
## Vanity
These types of metrics feel good to the people that are measuring them, may make us happy to see the number change, or generally give our ego a boost, but ultimately don't tell us very much. Examples of this may include:
- Product Backlog Health
- No. of Code Reviews
	- Completing 100 code reviews but missing 100 bugs doesn't provide a positive outcome.
- Number of units created
	- Creating defective or low quality still counts towards creation.
- Unit Test Coverage
	- Creating tests for the sake of seeing the percentage number increase actually has the potential to make it harder to make development progress without providing value.
- Website hits
	- Users navigating to your page may indicate some level of traction, but if 99% of those users never make it off the homepage it doesn't indicate success.
## Proxy
These metrics may indicate the potential for success but don't ultimately directly evidence success. Examples of this may include:
- No. of downloads for content
	- This does not show whether the content was valuable to the user, or if they accidently downloaded five copies.
- No. of items added to baskets
	- Items added but never purchased don't show success for an e-commerce business.
- Page Views
	- This may indicate that people are getting to the page you want them to, but if they don't perform the actions or consume the content you're intending them to it doesn't show success.
## Business & Customer-orientated Metrics
These are the metrics that should be focused on. They indicate some level of concrete and evidence based success for the product. This may include increase in revenue, customer retention, customer acquisition etc.

# Frameworks
## North Star
The North Star framework looks to provide guiding light for a [[product team]] to work against. The purpose of the framework is to help a team shape metrics that indicate whether the development they complete impacts the performance of their [[Product]]. 
### Product North Star
The Product North Star is meant to be the One Metric That Matters (OMTM). It gives insight into what matters above anything else at any point in time. Often, this may be a combination of Reach, Engagement and Frequency factors.

Example for how this could be applied for Netflix:
![[Netflix North Star Example.webp]]

Good North Star Metrics will also likely have three attributes:
1. It measures the moment that a customer finds value from your product
2. It represents the core of your product strategy
3. It is a leading (not lagging) indicator of a future business outcome the company cares about

Other examples:
![[Example North Stars.webp]]
### Key Influencers
To be able to measure progress towards our [[#Product North Star]] Metric on a more granular level, as sometimes changes we make won't have a big swing on our North Star immediately, we use Key Influencer [[Key Performance Indicators|KPIs]] to be able to see a more immediate effect on the product. In the example above, Reach, Engagement and Frequency would be examples of Key Influencers. To affect the amount of time spent streaming content, which is not specific to an individual but an aggregation of all time spent streaming, we have to affect one of three factors: the number of people watching, the average amount of time spent watching, or the frequency that a user returns to watch.
#### Example

Let's consider Booking.com as an example, assuming the North Star of "Number of nights stayed" has the Key Influencers of "Number of Bookings", "Number of Days Booked" and "Number of Returning Customers".

The [[Product Team]] has a [[Learning Test Cycles#Hypotheses|Hypothesis]] that sending out a newsletter on a daily basis with potential deals will increase the "Number of Nights Stayed" North Star metric. They develop their solution, deploy it to production, and monitor the outcomes of their work.

After a week they notice the "Number of Nights Stayed" has not increased, and so look further at their key influencers. They notice that the "Number of Bookings" the site has received has not changed, but that the "Number of Days Booked" has increased and the "Number of Returning Customers" has decreased. Based on this, the product team decide to investigate further and find that in providing a newsletter every day they have inadvertently upset their loyal and returning customers by over communicating. They also find that they've received more group bookings from people looking for deals they believe are ideal for more than four people.

With some further analysis, the [[Product Team]] understand that the average stay for four people and more is typically shorter than solo and duo bookers, but that the solo and typically book more regularly for longer periods. The team can now make a decision of whether this was a beneficial trade off to the business even if it didn't change the overall North Star. They decide to leave it and see if they can capitalize on the slightly different market or increase their solo bookers again.

After a month, the team has seen a minor drop in the Number of Nights Stayed and through investigation find out that their market of groups of four is much smaller than individuals and couples and so decide to unwind their decision to send newsletters daily.
### Levers
# De Beers
## Product Group 1
### Product North Star
Polished Product Production Cost E2E: Dollar per Carat ($/ct)
### Key Influencers
Average total polished yields of Xct: Average Yield (ct)
15-20% Overall Reduction in Manufacturing Pipeline time: Manuf. Pipeline Time (days)
Reduction in shipping costs in supply chain: Supply Chain Cost ($)
### Levers
Consistency hitting SKUs across STD, FIN, NOR based on demand profile: Failure Rate (%)
Obtain Parity with \$/pol.ct to current supplier: Cost (\$/pol.ct)
## Product Group 2
### Product North Star
Undefined
### Key Influences
Undefined
### Levers
#### [[Lagging Indicator|Lagging Indicators]]
- 85% uptime of the IoT Agent, excluding external conditions and factors
- 100% of pilot site Machines are operating with the IoT Agent
- 98% of messages sent by the machines are received by the IoT Agent
- 0% machine downtime due to the IoT Agent
- 90% of data generated during offline operation is recovered and sent for analysis
# Other Product Metric Examples
| **Metric**                                                            | **Definition**                                                                                                                                                                  |
| --------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Adoption                                                              | Understand whether the product is delivering its intended value                                                                                                                 |
| Stickiness                                                            | Understand whether users keep coming back and regularly engage with the product                                                                                                 |
| Acquisition                                                           | Understand the rate at which the product gains new unique audience members                                                                                                      |
| Retention                                                             | Understand the percentage of users who still use your product after initial use or installation. Can be done at both a product and feature level.                               |
| Growth                                                                | A combination of the Acquisition and Retention metrics, and therefore helps identify the reach and general success of the product                                               |
| Time to Value                                                         | The amount of time from the point a customer starts using the product to realising the intended value. The shorter, the better.                                                 |
| Top Feature Requested                                                 | Understand the desire of the audience through regularly requested features.                                                                                                     |
| Number of [[Learning Test Cycles#Experiments\|Experiments]] completed | Learning metric that outlines the completed experiments within the product team, and therefore the number of avenues that have been explored before settling on the chosen one. |
| Customer Drop-off rate                                                | Understand at which point customers disengage with the content they are being provided                                                                                          |
| [[Net Promoter Score]]                                                | Understand the loyalty of your customers                                                                                                                                        |

# Sources
[The One Metric That Matters](https://growwithward.com/one-metric-that-matter/)
[North Star Metrics](https://growwithward.com/north-star-metric/)
[Measuring the right north star](https://www.mindtheproduct.com/measuring-the-right-north-star-metric/)
[KPIs every product team should measure](https://www.pendo.io/product-led/8-kpis-that-every-product-team-should-measure/?&utm_source=mtp&utm_medium=display&utm_campaign=mtp-top-kpis-q3)
[Types of Time to Value](https://www.paddle.com/resources/time-to-value)