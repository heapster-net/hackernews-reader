# Hacker News viewer

Your task is to create [Hacker News](https://news.ycombinator.com/) reader.

Hacker News is an amazing platform for sharing news from technology world. Despite the impact of the HN, the site remains quite simple and without any additional besides the standard functionality.

Your goal is to create Flask app that will crawl the Hacker News page, cache its results and then provide easy-to-use interface with additional functionalities.

## Part 1 - Adventure begins
Create Flask App that will scrap the articles from the main page of the Hacker News and save them to the database. Create simple interface which will display those articles.

Add ability to change the order of the articles - by number of points, by number of comments, by creation date.

The scrapper should run only once, when the database is empty.

### Libraries / Frameworks to be used:
- Flask
- SQL Alchemy
- SQLite (for quickstarting)

## Part 2 - Did something move?
Now let's add some dynamism to the app. Add a button "Update Entries" to the page, that will remove all the entries and run the scrapper again.

## Part 3 - Wow, it's changing!
The app is working like a charm, but it is not the best solution to remove all the old entries when we update the data. Maybe better solution would be to just add new and update the old one instead?

Rework the "Update Entries" button to scrap and update the data instead of replacing it completely. If the entry is new, just add it, if the entry exists, replace it's data with the new one!

## Part 4 - Searching
Now we should add the searching mechanism. Let user type the searching phrase and return him only the articles that have this phrase in the title.

## Part 5 - Let's dive deeper
Currently, we are scrapping only the first page of the hacker news. But sometimes really fascinating articles are never making the way to the page 1, we will be never be able to read them :(. Let's fix that. Extend the scrapper to search through *n* first pages - make the number configurable in the code (create a constant at the top of the file or in the configuration file if you have any).

## Part 6...
More parts will be available in the future :)