# Initiatives & Themes
- A long-term strategic objective to achieve an organisational goal
- Aim for a lifecycle of between 1Q and 4Qs
- Capital Expenditure or Operational Expenditure depending on the type of work
# Epic
Epics Deliver a high level piece of value to a customer. This may take more than one quarter to deliver, but should regularly close as progress is made. Long running Epics reduce transparency for [[delivery]] and should generally be avoided.

Epics are either made up of multiple features, stories or both. They are the high level goal
- A group of work items that primarily break down into Stories and Enablers to deliver customer value
- Aim for less than 1Q [[delivery]].
	- If too large for 1Q [[delivery]], requires splitting
- Capital Expenditure of Operational Expenditure depending on the type of work
# Feature
A rollup of multiple [[user stories]] that achieve a specific piece of value. This is a more granular Epic and in some organisations may just be called an epic. The aim for a feature is to close it rapidly, ideally within one quarter. If this is not an achievable timeframe then the Feature should be broken down to achieve this, and could potentially be considered Epic size in its own right. This terminology comes from [[Scaled Agile Framework for enterprise|SAFe]], Features consist of the customer facing value that will be used daily. Though the work associated to the development of a feature might constitute a feature of a [[product]], it is likely that the work required to introduce an entirely new capability would not fit into a Feature-sized piece of work.
# User Story
[[User Stories]] make up the main part of most [[Scrum#Product Backlog|Product Backlogs]]. They outline conversations that have taken place between individuals, whether between customer and [[product team]] or between members of the development team. They can be of all sizes, and will be regularly updated as more is learned about the need.
## Enabler
At times there may be the need to do a purely technical piece of work that does not contribute anything to a customer. This should, generally speaking, be avoided where possible and rolled into a User Story that delivers customer value as regularly creating Enablers can lead to an excuse for horizontal slicing within a team. There are valid examples of this where enough of a slice of value is delivered to the development team that it warrants an exception. For instance, setting up a new service in a software [[product]] may include the infrastructure, software foundations and [[Quality Assurance|testing]] that the empty service works as expected before any business logic is added. It "enables" all other feature work to be carried out in vertical slices.
# Debt
Debt is built up by people while developing any piece of technology or process, whether intentionally done as a choice, or unintentionally done due to lack of foresight, change in direction or aging processes/technology. If debt is not maintained and regularly paid down then 
## Technical
These work items illustrate the debt incurred through the development of a [[Product|product's]] technology. This may be as a result of surrounding technologies progressing and not being kept up-to-date within the [[Product]] being developed, such as code libraries in [[Software Engineering]], or through obsolescence, such as a component no longer being manufactured by a supplier.

Technical Debt may equally be incurred due to cutting of corners, either intentionally or unintentionally due to factors such as project deadlines.

Finally, Technical Debt may be uncovered after development has completed due to legacy issues being identified. Where a component was developed with one purpose, and changes made to the surrounding components without maintaining the all dependent infrastructure, it may become apparent that the legacy solutions are no longer fit for purpose and need to be recreated or updated. 
## Process
Where technology development comes with its potential for debt, any other part of a business may also be impacted by their previous decisions in the form of Process Debt. Where something is so laborious or challenging to complete due to the decisions made be predecessors, process debt could significantly increase the operation time for completing those tasks.
# Bug
Also known as defects, bugs are unintentional faults in systems that negatively impact the experience of a customer or user. Dependent on the severity of the impact, it may be a nuisance or it could catastrophically impact the experience of that user.
## Pre-release
These are found prior to releasing to production, and are the most acceptable variety of bugs. They will have been identified and eradicated before the solution reaches a production environment, thereby ensuring the best experience for the customer after release. Catching these type of bugs before production is far cheaper than post-release
## Post-release
These are found once the software has already gone live. As release processes are historically expensive due to investigations, development work, support calls and customer communications eating up people's time, these are generally to be avoided as much as possible. The rough rule of thumb used when [[Software Engineering|Software Development]] more regularly promoted releases through a hierarchy of environments was that each environment a bug passes through adds a zero to the cost to resolve it. Depending on the context of a business and the model it uses for its [[Customer Support]] or [[Service Level Agreements|SLAs]], it will likely pull members from multiple departments and multiple seniority levels into play. As the most expensive commodity of any business is the time of its employees, the effect observed by post-release bugs is easily quantifiable by the amount of time and number of people involved in resolving these types of issues.