# Jellyfish Project Two Pitch

### Problem
When traveling, one’s information for the trip can get scattered across many
different apps making it quite hectic to get a simple overview of their plans.
The flight details will be on the airline’s website or app, while lodging details
are within the inbox. It gets exhausting when this is done repeatedly, not to
mention, the additional time it takes to search for that one specific email
regarding the AirBnB booking or the one with the confirmation number to lookup
flight details.

### Appetite
This problem is straightforward and it's important to keep in mind that the solution should not be overcomplicated. The goal now is to create a simple web system where users can log in and view all their upcoming trips with each of its own information. The end product must be straight-forward, clean, and as simple and smart as possible. We want the users to feel that all the important data can be found within the web service we are trying to build.

Following a six-week term to develop this project, the bare minimum for the full system includes:
- Displayed information of scheduled flight (involves flight data API)
- A clean and well-structured interface to display trip information
- A non-exhausting form to fill-in the details of the trip

### Solution
My solution is to create a system that would help users view their trip details and compile it in one place for easy access. The important thing about this is making sure that the information is displayed in the simplest and most intuitive manner. The system will allow the user to enter information about the trip with forms. There are three main groups of information when it comes to travel plans: transportation, accommodation, and itinerary. For this project, the focus will be towards transit and lodging. Adding an itinerary of places to visit will be set aside for future development.

Information will also be uploaded to a database to enable users to view their information across devices.
A flight API [AeroDataBox](https://rapidapi.com/squawk7000/api/aerodatabox/pricing "API link") will be used to view the flight details and its status.

#### Home and Trip Overview
On the left is the initial view of the system once the user has logged in. When a trip is clicked, the screen will display all the information about the trip. Past trips can be viewed below the upcoming trips.

![Home screen](https://user-images.githubusercontent.com/42617851/73246002-76fe2d80-41a5-11ea-81d9-5b69625eefec.png)

#### Creating a Trip

This is the form with the basic fields to be filled by the user in order to start creating a trip.
![Form](https://user-images.githubusercontent.com/42617851/73246003-7796c400-41a5-11ea-91a8-b86988887ae5.png)

#### Transportation

For transit, users will be able to select among road, rail, or air. If they choose air, they will be asked to fill in their flight details which will enable the system to connect to an API that will collect all other information. Their date of departure and flight number is needed to do this.
![Transit details](https://user-images.githubusercontent.com/42617851/73246004-7796c400-41a5-11ea-96eb-b7188b964749.png)

#### Accommodation

For accommodations, information to be asked from the user would include: name, address, and their check-in and check-out date and times. If their accommodation type is an Airbnb, an additional field for the passcode would be displayed (most Airbnb stays are equipped with electronic locks). Accommodation type "Other" would just display a text box for notes. This type would be the choice if users are planning to stay with their family or friends.

![Transit details](https://user-images.githubusercontent.com/42617851/73246006-7796c400-41a5-11ea-917c-1a980f2a77b8.png)

### Rabbit Holes
- 250 requests per month to AeroDataBox is enough to develop the system, otherwise the team would pay $5 a month for up to 5000 requests a month.
- How do we implement account authorizations (user logins)?
- Past trips will not be deleted from the database, however they will be minimized and will be put below upcoming trips.
- For road and rail, the input for the departure and arrival location will be text fields. We will not implement a select list nor an auto-fill.
- There will only be one transportation record per trip. Multiple transportation records will be addressed un future developments.

### No Go
- No calendars
- No drag-and-drop features
