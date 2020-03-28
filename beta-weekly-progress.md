# Weekly Progress
## Report for March 26
We have created a new Github repository for our beta cycle in order to separate everything and see new reiterations of what we are doing? All the previous files from the alpha cycle have been copied into the beta repo.

We have made the switch from SQLite3 to mySQL. We wanted to ensure that post-alpha release we would have a more stable database to work with as we continue to make new releases and go through new cycles.  We have created a to-do list based off of Stolley’s feedback on our alpha release and our group members’ thoughts.

More specifically, we are in the process of fully implementing Passport to authorize sign-in and registration with Google Authentication. We are now able to get user’s information which includes their full name, profile image, and email address. With the feedback we received from Stolley, we will be tweaking our routers to improve code flow.

We will also be moving constant variables to our .env file. In the case of our flight-data.js, we’ll be applying this to variables: hostname and x-rapidapi-host.

Moving forward we will be meeting with Professor Stolley sometime next week. We will also be scheduling our own meetings to discuss how we are going to move forward to complete the to do list.
