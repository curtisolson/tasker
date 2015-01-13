#Tasker Repository
This is a collection of tasker projects, profiles, tasks and scenes built by Curtis Olson. I've borrowed heavily from other tasker zealots and as much as possible, I will credit those people.

I find scenes painful to develop, so they are either really ugly or stolen from someone else.

Feel free to copy, use, modify for any reason. 

## Project: Driving
This containts all the tasks I've set up to use while driving. I use CarHomeUltra to create a (mostly) hands-free interface.

Not included in this project is a context manager which runns different tasks depending on if I'm at home, work, driving or unknown.

###Prerequisites
Apps and plugins used in this project.:

- Audible: Audio book app
- AutoInput: Tasker plugin
- AutoContacts: Tasker lugin
- CarHomeUltra: Car dock app
- PocketCasts: Podcast app
- Slacker: Streaming music app

##Tasks
###Audible Play
Using an input paramater, play any audio book downloaded on the phone. Since Audible doesn't have a way to play a book using an intent, I use Autoinput to simulate input events to navigate and play. Task accepts an input paramater for the name of the audio book.

###Audible XXXXX
Where XXXX is the title of the audiobook. Tasks simply call the "Audible Play" task and pass in a book title.

###Call Queue
Task which displays a menu of contacts that I want to call from the car. The idea is to add phone calls which can easily be made while driving. 

This task will show a scene with a lit of contacts with nickname "Call Queue". If you select one of the contacts, their phone number will be dialed and a large scene with the info from the website field will be shown. There is a note field in contacts, but AutoContacts doesn't (yet) return that field. I put notes in there that I may need during the call, like account number.

Be aware that AutoContacts imports a copy of your contacts, so a refresh will need to happen for a new caller to be added to this list.

###PocketsCasts Play Playlist
Using an input paramater, play an entire playlist. 

###PocketsCasts Play Podcast
Using an input paramater, play any podcast. This task picks the first episode available for play if there are multiple. 

###PocketCasts XXXXXXX
Since step task that just call Play Playlist or Play Podcast and pass in a name to be played.

###PocketCasts Mark As Played
Marks a playing podcast as played and deleted it. This is used if I start a podcast but decide it stinks and want to move one.

###Slacker Play Station
Using an input paramater, play any Slacker station you have alrßeady added to your music list. I use Slacker Free which has a lot of interuptions and pop-ups. I may have to add more AutoInput UI Query to handle different interruptions.

### Slacker XXXXXXX 
Since step task that just call Slacker Play Station and pass in a name to be played.