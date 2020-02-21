# Weekly Progress

## Week of February 17

This week, we took what we learned from Stolley’s lecture on using git and refreshed our memories. We also created a reference sheet on using Git so everyone in the group has an accessible reference based on Stolley’s workflow. Additionally, following what Stolley taught us, we have added rules/restrictions to who is allowed to push commits. Now, a commit cannot get pushed/merged without at least everyone’s approval in the group. Furthermore, we have established that we will use feature branches as we work to organize everything nicely. 

We took this week to familiarize ourselves with using the API and studying its syntax. We will continue our work with this tomorrow as we decide what information we will be asking the user regarding their flight and what data we will be storing from the API. The group meeting with Stolley led us to opt for an SQL database rather than MongoDB. In the context of our project and the data we will be storing for each user, we found that the logic pattern fits better with a relational database instead of a non-relational one. Stolley has also mentioned the use of SQLite as a database. We’re not familiar with this, so we are looking into its implementation and its difference from MySQL. Because we will be going for the SQL database, we are going to pinpoint what our data structure will look like. We will be holding our weekly friday meetings to discuss our next steps.

Our team had a slight bump in the road since we felt like things weren’t fully “clicking” together and couldn’t see the full big picture. Because of this we had a hard time taking our first steps since we didn’t know which direction to approach it. The meeting last Monday was helpful and Stolley advised us to simply start coding from both ends—which we are taking to heart. This week we will start focusing on implementing Express and do some practice work with it. We will also start to write out code in HTML and CSS for what the trip fill-out form would look like based off of the big marker sketches from our pitch. This will help us have a better understanding of the user flow and the necessary fields and data needed to match the user’s need. JavaScript will be integrated in later weeks, after we have most of the interface solidly built.

As for our web application name, we have decided to hold off on choosing one until the beta cycle. So for our alpha cycle, we can focus on working on its core functions and worry about other details in the next cycle per our group’s agreement on what will get done during this alpha cycle.


## Week of February 10

We have spent this week refining our idea in response to Professor Stolley’s feedback.

We have decided to not focus on accommodations during the alpha development cycle in an effort to scope-hammer our system. Instead, this phase will focus on building the core feature which is the transportation information of the user’s travel. An update to our pitch: we will allow users to have multiple instances of transportation per trip. As mentioned in our pitch documentation, we have already found an API where we will pull in flight data from and users will be able to input other modes of transport that they will be using themselves.

We are also looking into the implementation of user logins into our web application and how this would relate to the database structure.

We have made a few decisions regarding the components of our architecture. We decided we will be using NodeJS as our server-side scripting language with Express as our framework. In regards to our database, we will utilize MongoDB. And just to reiterate, our front-end languages will be in HTML, CSS, and JS.

We have created a new repository strictly for the alpha cycle called alpha-jellyfish (link to repo here: https://github.com/jellyfish-wsi/alpha-jellyfish). The previous GitHub repository (jellyfish-p2) only contains our project pitch and will also be used to store our weekly progress reports.

Currently, we are deciding on the architecture pattern of our web application. The patterns we are currently considering are: layers pattern, shared-data pattern, and multi-tier pattern. Our goal is to decide by Friday which of these will suit our project best during our meeting.

On a different note, we are also currently brainstorming ideas on what to call our web application.
