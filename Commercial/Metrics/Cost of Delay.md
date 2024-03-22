---
tags:
  - MathFormula
  - Commercial
  - Prioritisation
  - Metrics
  - Resources
---
# About
This is the value associated with lost [[revenue]], lost opportunities, increase [[risk]], and customer respect among other critical factors of a business. Put simplistically, cost of delay is the expected profit divided by the duration to realise that profit.
$$ Expected Profit / Development Duration $$
This can then be used to identify the prioritisation of [[delivery]] based on the value associated with each item. 

|           | **Project Duration<br>(Weeks)** | **Expected Weekly Profit** | **CD3 Value**    |
| --------- | ------------------------------- | -------------------------- | ---------------- |
| Project 1 | 2                               | 5,000                      | 5,000/2 = 2,500  |
| Project 2 | 4                               | 30,000                     | 30,000/4 = 7,500 |
| Project 3 | 8                               | 50,000                     | 50,000/8 = 6,250 |
| **Total** | **14**                          | **85,000**                 | **N/A**          |

The higher the Cost of Delay value, the higher economical impact it will have as return on investment is faster.

## Scenarios

<html>
	<body>
		<Table style="width: 100%">
			<tr>
				<th colspan=14 style="text-align:center;">Weeks</th>
			</tr>
			<tr>
				<th style="text-align:center;">1</th>
				<th style="text-align:center;">2</th>
				<th style="text-align:center;">3</th>
				<th style="text-align:center;">4</th>
				<th style="text-align:center;">5</th>
				<th style="text-align:center;">6</th>
				<th style="text-align:center;">7</th>
				<th style="text-align:center;">8</th>
				<th style="text-align:center;">9</th>
				<th style="text-align:center;">10</th>
				<th style="text-align:center;">11</th>
				<th style="text-align:center;">12</th>
				<th style="text-align:center;">13</th>
				<th style="text-align:center;">14</th>
			</tr>
			<tr>
				<th style="border:none;" colspan=14/>
			</tr>
			<tr>
				<th style="border:none;" colspan=14/>
			</tr>
			<tr>
				<th style="border:none;" colspan=14 />
			</tr>
			<tr>
				<th colspan=14 style="text-align:center;">All at once</th>
			</tr>
			<tr>
				<td style="text-align:center;">x</td>
				<td style="text-align:center;">x</td>
				<td style="text-align:center;">x</td>
				<td style="text-align:center;">x</td>
				<td style="text-align:center;">x</td>
				<td style="text-align:center;">x</td>
				<td style="text-align:center;">x</td>
				<td style="text-align:center;">x</td>
				<td style="text-align:center;">x</td>
				<td style="text-align:center;">x</td>
				<td style="text-align:center;">x</td>
				<td style="text-align:center;">x</td>
				<td style="text-align:center;">x</td>
				<td style="text-align:center;">x</td>
			</tr>
			<tr>
				<th style="border:none;" colspan=14/>
			</tr>
			<tr>
				<th style="border:none;" colspan=14 />
			</tr>
			<tr>
				<th style="border:none;" colspan=14 />
			</tr>
			<tr>
				<th colspan=14 style="text-align:center;">Shortest First</th>
			</tr>
			<tr>
				<td colspan="2" style="text-align:center">Project 1</td>
				<td colspan="4" style="text-align:center">Project 2</td>
				<td colspan="8" style="text-align:center">Project 3</td>
			</tr>
			<tr>
				<th style="border:none;" colspan=14 />
			</tr>
			<tr>
				<th style="border:none;" colspan=14/>
			</tr>
			<tr>
				<th style="border:none;" colspan=14 />
			</tr>
			<tr>
				<th colspan=14 style="text-align:center;">Most Valuable First</th>
			</tr>
			<tr>
				<td colspan="8" style="text-align:center">Project 3</td>
				<td colspan="4" style="text-align:center">Project 2</td>
				<td colspan="2" style="text-align:center">Project 1</td>
			</tr>
			<tr>
				<th style="border:none;" colspan=14/>
			</tr>
			<tr>
				<th style="border:none;" colspan=14/>
			</tr>
			<tr>
				<th style="border:none;" colspan=14 />
			</tr>
			<tr>
				<th colspan=14 style="text-align:center;">Highest Cost of Delay</th>
			</tr>
			<tr>
				<td colspan="4" style="text-align:center">Project 2</td>
				<td colspan="8" style="text-align:center">Project 3</td>
				<td colspan="2" style="text-align:center">Project 1</td>
			</tr>
		</Table>
	</body>
</html>

### Scenario 1
Prioritised by ascending project duration, completing the shortest project first and building incrementally through to the longest.

|           | Project Duration<br>(Weeks) | Expected Weekly Profit | Cost of Delay                  |
| --------- | --------------------------- | ---------------------- | ------------------------------ |
| Project 1 | 2                           | 5,000                  | 2 * 5,000 = **10,000**         |
| Project 2 | 4                           | 30,000                 | (4+2) * 30,000 = **180,000**   |
| Project 3 | 8                           | 50,000                 | (8+4+2) * 50,000 = **700,000** |
| **Total** |                             |                        | **890,000**                    |
This calculation is completed through calculation of the loss of profit due to lead time to build. Projects 2 and 3 must wait for the other projects to finish first and then must incur their own cost during development.
### Scenario 2
Prioritised by descending project duration, completing the longest project first. 

|           | Project Duration<br>(Weeks) | Expected Weekly Profit | Cost of Delay                |
| --------- | --------------------------- | ---------------------- | ---------------------------- |
| Project 3 | 8                           | 50,000                 | 8 * 50,000 = **400,000**     |
| Project 2 | 4                           | 30,000                 | (8+4) * 30,000 = **360,000** |
| Project 1 | 2                           | 5,000                  | (8+4+2) * 5,000 = **70,000** |
| **Total** |                             |                        | **830,000**                  |
### Scenario 3
|           | Project Duration<br>(Weeks) | Expected Weekly Profit | Cost of Delay                |
| --------- | --------------------------- | ---------------------- | ---------------------------- |
| Project 3 | 4                           | 30,000                 | 4 * 30,000 = **120,000**     |
| Project 2 | 8                           | 50,000                 | (4+8) * 50,000 = **600,000** |
| Project 1 | 2                           | 5,000                  | (2+8+4) * 5 = **70,000**     |
| **Total** |                             |                        | **790,000**                  |
### Scenario 4
If a decision is made to work on all 3 projects simultaneously then the likelihood is they all complete around the same time. This will mean the development time takes 14 weeks with a weekly cost of 85,000. Multiplying these two together, we define the cost of delay as 80,000 * 14 = 1,190,000.

## Compare Scenarios
Comparing each, it is clear to see that the most profitable choice is to prioritise by the CD3 value.

| Priority Criteria | Cost of Delay |
| ----------------- | ------------- |
| No Priority       | 1,190,000     |
| By Duration       | 890,000       |
| By Value          | 830,000       |
| **By CD3**        | **790,000**   |
## Types
### Standard
This is as described above.
![[cost-of-delay-standard.webp]]
### CoD Tied to Fixed Date
An example of this is in hitting an SLA. The cost of delay is non-existent or low until a specific time, at which point its cost grows exponentially. This may be due to fines placed on the SLA at certain levels which could be either by refund or by negotiated fee.
![[cost-of-delay-fixed.webp]]
### CoD Tied to Urgency
An example of this is launching ahead of a competitor or disruption in the sector. The cost increases rapidly until a fixed and constant amount that reflects the impact on the organisation against the market.
![[cost-of-delay-urgent.webp]]
# Resource
https://businessmap.io/lean-management/value-waste/cost-of-delay