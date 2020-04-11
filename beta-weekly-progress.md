# Weekly Progress
## Report for April 9

We have successfully gotten our database to connect. It also doesn’t hang now after connecting because it closes itself afterwards. Having added the database connection, everyone has it hosted on their own local environments as well (as mentioned in last week’s report). Our group is implementing *Sequelize* on our app to aid us in data migration and CRUD operations. *Sequelize* is an Object Relational Mapper which works with MySQL and NodeJS and makes the database code more efficient. We currently have a user hardcoded into our database just to test out whether it was working or not. Just like when we were using SQLite3, we still have 3 tables: Users, Trips, and Transportation. 

Connecting and closing the database. 
![Database](screenshots/db1.png)


RUNNING `npm run dstart` 
![Database](screenshots/db2.png)


After starting up mysql
![Database](screenshots/db3.png)


The image shows our three tables: Transportation, Trips, and Users 
Jane Doe is the hardcoded user. 

In addition to that, we tagged our first beta pre-release for the complete implementation of Passport. 

Now, we can proceed with adding the user credentials (from the user authentication) to the database, as mentioned above. Once we’ve connected the user authentication, we will be doing another patch release. 

On the server side, we are having trouble connecting our domain to our HTML file on our server. Currently, we have created a new directory in the nginx directory called `jellyfish-web.us.conf.` We have tried to reboot the server to see if this would help but it didn’t help, so we are going to continue to troubleshoot. 
This is what’s currently inside of jellyfish-web.us.conf

![Server](screenshots/server.png)





## Report for April 2
Going off on Wednesday's lecture our group has decided to go with Linode Server for our web application. We all pitched in and purchased a basic server. Root has been disabled and everyone in the group has access as their own users for the server. The main user that we are going to run on is diana@45.79.41.156.

![Linodes](screenshots/linode.png)

On this server we have installed git version 2.20.1 and NodeJS. To add on to that, we have also enabled the firewall. On our SSH server, we installed fail2ban to protect our server. Nginx has been configured to allow both http and https on our pages. We will be running Nginx on Debian 10. In terms of maintenance with our server, we have made the decision to shut it down for now in order to save money and keep it secure. There was an issue trying to add authentication keys so we plan on working on adding them to keep our server more secure. 

![Terminal](screenshots/terminal.png)

We have also purchased a domain: jellyfish-web.us on active domain. When the server is up and running you would be able to use this link or the IP provided by Linode to reach our web server which in this case is nginx.

![nginx](screenshots/nginx.png)

GitHub was alerting us of security risks with our project with the dependencies we had. We discovered that a few dependencies weren’t updated and have since resolved the issues by updating everything in our package-lock.json to the latest version. 

As mentioned in a previous comment on Basecamp from last week’s report, we have fully implemented Passport JS and have made improvements. Besides being fully functional, we have also tidied up the routers, and authentication functionalities are now under the `/auth` path. In addition to Passport, we’ve also included `connect-ensure-login` as a dependency. This is a light middleware which safeguards pages from being accessed if there is no user logged in. We had a slight hiccup with implementing this since a failure would redirect to the wrong page. However, we’ve resolved this and everything works fine now! We’ll be making a minor release for this.

The next step in terms of user authentication is to have the user credentials match or registered to the database. However,  for our database, we are still in the process of transitioning from SQLite3 to mySQL. We are trying to get a script running to connect to a database that will be created to hold the user’s information. When we have the database connection, everyone will have it on their local environments. Then, we can proceed with adding user credentials for user authentication as mentioned above. 

For the server we need to add a file to track the specific parts of etc/nginx and continue to config our Nginx. We will also be adding certbot to allow users to use https (to avoid the “Not secure” message).

As mentioned in our previous report, this is a list of the milestones we have planned, with each of them potentially being a minor release:

- Connecting the database to the web application (GET and POST of user information and trip data)
- Completed implementation of Passport JS
- Significant progress on interface (UI/UX)

## Report for March 26
We have created a new Github repository for our beta cycle in order to separate everything and see new reiterations of what we are doing? All the previous files from the alpha cycle have been copied into the beta repo.

We have made the switch from SQLite3 to mySQL. We wanted to ensure that post-alpha release we would have a more stable database to work with as we continue to make new releases and go through new cycles.  We have created a to-do list based off of Stolley’s feedback on our alpha release and our group members’ thoughts.

![To-do list](screenshots/03-27-01.png)

More specifically, we are in the process of fully implementing Passport to authorize sign-in and registration with Google Authentication. We are now able to get user’s information which includes their full name, profile image, and email address. With the feedback we received from Stolley, we will be tweaking our routers to improve code flow.

We will also be moving constant variables to our *.env* file. In the case of our *flight-data.js*, we’ll be applying this to variables: *hostname* and *x-rapidapi-host*.

Moving forward we will be meeting with Professor Stolley sometime next week. We will also be scheduling our own meetings to discuss how we are going to move forward to complete the to do list.

Here is a list of the milestones we have planned, with each of them potentially being a minor release:

- Connecting the database to the web application (GET and POST of user information and trip data)
- Completed implementation of Passport JS
- Significant progress on interface (UI/UX)
