# groupprojectone
Our first group project with James Tre Akhila Patrick

Project 1 Group 2
Group Members :- James Winkle, Akhila RK, Tre A-D, Benjamin (Patrick) Register

Project Description :- Aptly named The Road Trip App, this web application provides the user, valuable information required to embark on a road-trip, namely Maps, Directions, Weather at the destination and some Music for the road.

Extensively used APIs :- 
1. Google Maps API services: 
- a. Geocode API
- b. Directions API
- c. Distance Matrix API
2. Spotify API
3. Open Weather Map API

Tech Used :-
HTML, CSS, Bootstrap, Javascript, JQuery, JSON, AJAX, Git, Heroku, Firebase


Detailed Description:-

1. The Map and Directions services are provided by AJAX calls to Google Maps API with Google Maps Directions API providing the route, and Google Maps Geocode API providing the map to display the route. Google Maps Distance Matrix API call was used to get the exact duration of the trip, which will be used to display the tracklist.

2. A Traffic layer on the map displays traffic info and areas of congestion over the course of the trip.

3. For music, the user's favorite artist choice is taken as input, and queried against the Spotify API to get an artist ID. The artist ID is then used to make another AJAX call to get a list of related artists IDs which are then pushed into an array of artist IDs that include the original artist ID also. This is then used to fetch 10 tracks per ID using another AJAX call. All of the tracks are then pushed to an array and shuffled, creating the tracklist that is displayed. On click of a track, the song begins playing on an iFrame from Spotify, by appending it to the html. The cool feature here is the use of the duration returned by Distance Matrix API to trim the duration of the playlist.

4. The weather is displayed using Open Weather Map API. It takes in the destination entered and returns the weather details in a JSON that was traversed to populate the weather fields on display.

5. Firebase was used to populate a field to display how many times the site was viewed/ used. Also stored in Firebase is an object per trip with the artist entered by the user, the destination they intend to go to, and the timestamp. This will prove useful for a future development idea.


Improvements/ Future additions:- 

1. The original idea for playing music was to use the tracklist to create a playlist in the user's Spotify account, which was challenging due to the current knowledge we possessed, hence it has been slated for future improvements. The idea is to let the user login to the Spotify through the app's login form, fetch the user's info and push the tracklist to a playlist titled 'RoadTrip#'. This should enable the app to use the Spotify Play widget that instantly plays the songs non-stop without any user presses/clicks (which serves the purpose of this project i.e. no user input required on the road. Everything is set before start of trip.)

2. In addition to the Traffic layer, a Heatmap layer to display potential accident prone areas and toggle checkbox buttons may be implemented so the user can take each layer off when not required.

3. Analytics has been shelved as a future improvement. The start of this is seen in the number of views using Firebase connections. Using the data stored in objects per trip, (see Detailed Description point 4.) a chart/graph can be plotted that shows popular artists over a period of time. Another graph can show popular destinations for road trips. This will be housed within the Analytics panel at the bottom. 

4. Creating the analytics section poses the question of whether the data needs to be public or private to a set of distinguished users. This can be solved using authentication for admin users who alone will be given access to view the Analytics panel. Or it could be made public. This is yet to be decided upon.
