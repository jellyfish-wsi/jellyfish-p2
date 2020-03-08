# Weekly Progress
## Week of March 2

After the lecture about APIs on February 26, we have been working on connecting our flight API. Like we mentioned in our previous progress report, our API will pull the information of the user’s flight (e.g departures and arrival times, flight status, etc). We noticed that our API offered four different types of requests for Node.js. After consulting with Stolley, we are going to go with the native HTTP library for Node.js. We have inserted the function provided by our API host to connect to the flight API. Though, we still need to declare the API key on our own local environments. We’ve setup Mocha for project testing. 

We are also in the process of starting up SQLite3 using the lecture video from this week. It has been added as a dependency in our package.json file. Currently our group is applying what we learned in our previous lecture about databases to guide us to make the proper connection between our project and our database. We created a folder called db to keep all the code related to the connection there.

We are working on modeling our relational database within SQLite3. So far, we are certain that we will have a Users and Trip table. For the Trip table, the columns will consist of: trip_id, name, start_date, return_date, and transport_mode. In terms of the Users table, it will have user_id, name, and email. The final table we will have is transportation where we will focus on more specific details about the trip. The columns will consist of: trip_id, company_name, mode, status, and seat. 

Throughout the week Dasha continued her work on carrying out the Google authentication and successfully got it to work. We have only applied it in its most basic form, so now we are looking to see how it would fit into the structure of Node.js. We plan to implement Passport (npm module) and use the passport-google-oauth20 as the strategy. With this, we will be able to authorize user accounts and create sessions as well. 

We will also be creating a confirmation page for the users to view all the information they have entered when they create a trip. Later on we'll be adding form validations to make sure the user filled out all the requirements for the trip. 


## Week of February 24

For this alpha stage, we have decided that we will be asking the users for a custom name of their trip, where their trip will be, and the dates of the trip (from x date to x date). Following that, they are then able to input what transportation method they will use. If their mode of transportation will be by road (driving) or rail (train), they are able to input their own information as a string. However, if they choose the mode as air, that’s where our flight API will come in. From there, they will enter the flight number and the API will pull in the information for our users. Basically the flow of data from the API will consist of departures and arrivals, flight status by flight number and date, flight departure dates by flight number in a range, flight status by just flight number, flight departure dates by flight number, and flight delay stats by flight number. 

Dasha was focused on the implementation of Google OAuth. For some reason, we kept hitting up an error where we would receive an error message that said “the page’s settings blocked the loading of a resource.” Dasha is trying to resolve this but after two days of working on it, we haven’t found the issue yet. We’ve followed the documentation on Google’s resource page, yet we keep on hitting this problem. We’re continuing our work on this and are learning as we go.

So far, we have the basic skeletal files down based off the Express JS framework and the lectures from February 10 and 12. We have also established a ‘create a trip’ form in HTML and will continue working on the front end aspect. We will be getting some basic CSS put down in the next few days so that we have something a bit more tangible to show for progress next week.

In regards to the database, we’ve been doing some reading on implementing this and have a list of resources we share among the three of us on Basecamp. We have no code for this yet, but we’re looking forward to the lecture regarding databases in next week’s lecture to help us with that.

As for now, we are going over Stolley’s demo on connecting to an API together and we will be replicating what he taught with our AeroDataBox API (flight) through RapidAPI. We’ve done some basic interaction with the API, now it’s just the matter of organizing the code well and fitting it into our setup.

As always, we are collaborating using Basecamp and our GitHub is https://github.com/jellyfish-wsi.

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

### Week of February 3

#### What We've Done:

We, as a group, have adjusted and finalized Dasha’s pitch from her Project One.
We have established Basecamp as our means of communication. A separate Basecamp
project has been created for all the group members as well. A GitHub organization
with the group repository is established. Each group member has their own personal
repository that they will be making pull requests from to the main group repository
to ensure nothing will get messed up without the entire team’s agreement.

#### What We're Doing:

We are currently thinking about what frameworks to use for our web app. We know
that we will use the three main languages to begin with: HTML, CSS, and JavaScript.
But anything beyond that we are currently unsure of.

#### What We're Going to Do:

We’re going to come up with meeting times, so we can discuss details and work on
the project together in person. We will also find time to have a one on one
meeting with Professor Stolley.
