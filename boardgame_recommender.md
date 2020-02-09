# Boardgame Recommender System and Web App

[Github project link](https://github.com/johnmburt/springboard/tree/master/capstone_2)

Recommender app deployed to Heroku (note: startup can be slow):


One of the problems that impedes consumer access to the boardgaming hobby is that there is an embarrassment of choices: it can be hard for a person to find the right game among the many thousands that are available. Good board game stores hire experts to recommend the games a customer might like, but many consumers prefer to shop online. This consumer pattern suggests a digital solution in the form of a web-based board game recommender system.

For my second Springboard Data Science Career capstone project I developed a functioning board game recommendation engine web app to help consumers find, research and purchase boardgames. This recommender could be used by an online boardgame store such as Amazon or Coolstuffinc.com. The system asks a user to list some games that they like, as well as optional filter parameters such as preferred genre, game difficulty (weight). Then the recommender will use those preferences to search for and select a list of game titles to present.

The recommender app has been deployed on Heroku: [

- [jmb-boardgame-recommender.herokuapp.com/bokeh_app](https://jmb-boardgame-recommender.herokuapp.com/bokeh_app)


## The simple search tab:

The first, and default, tab has minimal complexity: the user can only enter the games they like and click the recommend button. Behind the scenes, the code does some filtering of the recommended games based on metadata provided by the “liked games” list: particularly, the recommendations will reflect the range of game weight (game difficulty) of “liked games”, and mean game ratings must be above a threshold (currently 7.5). The recommender does reasonably well with these restrictions, but it always recommends the same games given the same “liked” list. To provide some variation, I introduced a small random factor into the algorithm so that every time the user clicks “recommend”, a different list of games will be presented.

<img src="images/projects/bg_rec_app_simple.png" width="500">