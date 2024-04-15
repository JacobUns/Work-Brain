---
tags:
  - RonJefferies
  - Agile
  - Practice
  - "#MikeCohn"
  - Resources
---
# About
User stories are a method of conveying conversations held with users or internally as a development team. The practice comes from [[Extreme Programming|XP]], 
## Structure
### Summary
### Story
### Acceptance Criteria
## Types
In the core definition of the practice for [[Extreme Programming|XP]], there is no differentiation between types of user story. In most organisations, this is completely fine and keeps the concept simple. In frameworks like [[Scaled Agile Framework for enterprise|SAFe]], however, there is differentiation between types of story to try and help the breakdown of work caused by interdependent teams.
### Feature User Stories
These types of story directly contribute to the value delivered to a user. Something a user touches at any point which provides them value, whether behind the scenes or at their finger tips, can be considered a feature user story.
### Enabler User Stories
To enable the breakdown of work into regularly deliverable chunks, and to break down cross-team dependencies, a team may be required to deliver stories that provide no user value but ultimately delivers value to the engineering team. An example of this would be setting up the foundations for a new set of infrastructure, including new [[Micro-service Architecture]], pipelines and [[Repositories]]

# Theory
## INVEST
## 3C's
The 3Cs is a concept to convey the most important parts of a user story. They are:
- Card
- Conversation
- Confirmation

The 3Cs are described by Ron Jefferies, the creator of [[Extreme Programming|XP]] to illustrate  
# Templates
Below are a number of examples that give potential templates for use when creating User Stories. In each, if an example is provided it will be based on a hypothetical example of a travel website.
## Persona-centric
The most common form of writing User Stories that is taught puts the persona at the core of the message. Users are the people who have problems that need to be solved by a [[Product]], so we use language that puts them front-and-centre in a development team's mind. 

As a... **[[Persona]]**
I want... **Proposition**
So that... **Value Statement**

Both Persona and Value centric approaches use pronouns to shift the reader's thought processes to be more empathetic. Mike Cohn explains that one of the things that made bands like The Beatles popular was their use of pronouns like I and You in their music, which took the listener into a mindset of empathy and imagination. Similar is true of this format of user story writing. By use of pronouns, we put the reader into a mindset of trying to empathise with the problem being experienced by the [[Persona]].

### Example
As a Solo Traveler
I want to be able to book a holiday with other solo travelers
So that I can have some companions to explore with without needing to book through a separate provider I don't trust
## Value-centric
There are some instances where it may be preferred to highlight the value over anything else. This may be personal preference by a [[Product Management|Product Manager]] or [[Scrum#Product Owner|Owner]], or it may be to reinforce the mindset of a [[Product Team]] to be looking to understand the why before they define the solution. 
### Template
In order to... **Value Statement**
As a... **[[Personas|Persona]]**
I want... **Proposition**

The first thing we read, and therefore the first thing we try and compute and understand as the reader, is the value we're looking to deliver. The components of this template are exactly the same as when we consider the [[Personas|Persona]] as the main focus of the reader, but the order is swapped to emphasize something else instead. 
#### Example
In order to ensure that I can travel without inconvenience and with a sense of control,
As a person with a disability that affects my mobility,
I want to be able to search for places to stay that offer the most accessibility for disabled people.
## Engineering-centric
When we look at [[Work Item Types#Enabler|Enabler]] or technical work items, we tend to regularly repeat the same [[Personas|Persona]] which is usually some variety on "As a software engineer". This becomes superfluous, and ends up diminishing the value of examples where the [[Personas|Persona]] is important as a result. To combat this, we can simply remove the [[Personas|Persona]] from the template. Alternatively, we could substitute it for some context as to the purpose of the work. Below are examples of these types of template:

### Template
#### Template 1
We want... **Proposition**
So that... **Value Statement**
##### Example
We want to create a heartbeat for the service we have deployed to the production environment
So that we can attach alerting and monitoring capabilities to it to improve our [[Service Level Agreements|SLA]] [[Key Performance Indicators|KPIs]] for product uptime
#### Template 2
Having... **Context**
We want... **Proposition**
So that... **Value Statement**
##### Example
Having created a shell service and deployed it to production as the foundations for our infrastructure,
We want to setup up our new service within our network infrastructure with a specific domain name,
So that anyone trying to access the service can do so without using an IP address and we can log any type of traffic to our monitoring solution with a sensible name that allows for easier debugging  
# Sources
[Mountain Goat Software - User Stories - Mike Cohn](https://www.mountaingoatsoftware.com/agile/user-stories)
User Stories Applied - Mike Cohn