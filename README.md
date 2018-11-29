# Train Timetable
You don't need to train your brain to figure out when your train is arriving; we'll do it for you!

![Train Engine](train-background.jpg "It's comin' right at us!")

## Resources Utilized:

* Firebase
* Jquery
* Moment.js
* Math
* Logic
* Google Fonts
* HTML
* CSS
* BootStrap


## How It Went

This project was a relatively straightforward in terms of ask: Using Firebase and Moment.js, create a way to populate a timetable of trains by gathering their Names, Destinations, First Arrival Time, & Frequency. My approach took the following path:


1. Set up HTML to display the timetable as it is populated
2. Create a form to gather data from the user, constraing where necessary
    * Customer required time be inputted in 24hr format.
    * Use dropdown menus so that only times from 00:00 to 23:59 are allowed.
    * I used JS and Jquery to create the dropdown forms instead of hard-coding them.
3. Upon user clicking submit, store data in Firebase
4. Using Firebase's on "child_added" function, populate the train timetable with train information.
5. At this point, we use moment.js to grab the current time.
    * I imagine moment.js has a better/simpler way to calculate time differences, but I had trouble navigating through their documentation and converting collected times into times that moment could recognize.
    * I converted the current time and the train arrival time into "absolute" time in minutes, and used that to calculate.
    * I considered cases where trains arrived very infrequently, and this project allows for trains to come as often as annually, although that seems ridiculous considering we measure frequency in minutes.
6. I then performed calculations to get the required outputs of next arrival time and minutes until arrival, which are two ways of displaying the same information.
7. Finally, I put in some logic for if trains arrive on the next day or days. I also added some rules to get times to display as "01" instead of "1".
8. Added some styling and a README.

### Thanks for checking it out!!