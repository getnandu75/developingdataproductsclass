Movie Charts
author: Raghuraman Nandakumar date: September 2015

Inroduction
This presentation will introduce the Movie charts webapp that was a Course Project for the Developing Data Products class of the Johns Hopkins University, hosted by Coursera.

Access to the application

Live version on ShinyApps
Code and data on GitHub
Movie charts can run in any modern browser, suggested resolution is full HD. Mobile devices are technically supported, hovewer, due to the nature of the charts, the app might not be that useful on small screens.

Movie Charts
Movie charts is a simple webapplication that visualizes some properties of the IMDB top 250 movies. The dataset used by the webapp also contains the Rotten Tomatoes (RT) data for those movies so comparisons between the two sites are possible.

Movie charts also offers (a very dummy) prediction tool for predicting movie earnings.

Functionalities
Ratings: IMDB and RT ratings can be visualized against each other or against release date of the movie. Bubble size of the chart is also customizable, it can correspond to IMDB/Rotten Tomatoe rating number or the Metascore. Lastly, the color of the bubbles also customizable, it can represent MPAA rating or release data (exact year or decade)
Box office: A simpler chart where box office can be visualized agains the IMDB or RT data or release date. Also a prediction tool can be used to predict box office earnings.
Data retrieval: Description and code describing how the movie data was acquired
Data and Data download: Online viewer and downloader for the movie data
Help / Manual: a simple help page
Technical details
Movie charts uses standard ShinyApp features, using fluidFlows on several tabPanels
Data is loaded from a local JSON that was acquired via the OMDB API. See Data retrieval menu in the app for more details
shinyAce library is used to display code
For the box office prediction, the simplest possible prediction is used by fitting a linear model (trendline) on the data and using that line to predict Y values for X values that are entered by the user
Charts are displayed using the googleVis package
This presentation is done in R Studio's R presenter (.Rpres)
