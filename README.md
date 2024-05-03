# pythonrecipefinder
Python Recipe Finder project that stores and takes user input into putting recipes into databases based off of SQL. 
Alternatively, this also supports a basic level of web scraping, in which a user can also store a recipe into this database through taking the recipe information and link.

In my Python main script, it is a written application named Recipe Finder, which allows users to interact with a recipe database through various functions within the main menu that I set up. 
The application offers options to search for recipes by name, add new recipes from a URL, view all recipes in the database, or create and add custom recipes manually. 
The search_recipes function searches the database using a user-provided name and displays any matching recipes. 
In add_new_recipe, users can add recipes by providing a URL, which is scraped for recipe information that is then added to the database. 
The view_all_recipes function lists all recipes stored in the database. The `create_recipe` function allows users to enter a recipe name, instructions, and ingredients manually, which can be validated and then added to the database. 
I also integrated some error handling to manage exceptions that may occur during recipe addition or URL scraping. 
This design utilizes several classes, including RecipeDatabase, IngredientManager, IngredientValidator, and other utility classes, to manage recipes and ingredients effectively.

To elaborate on the web scraping side, the web recipes script I wrote is designed to extract recipe information from a webpage specified by a URL with the function scrape_recipe_info. 
This function utilizes the requests library to fetch the webpage content and the BeautifulSoup library from bs4 to parse the HTML content. 
It specifically looks for the recipe name and description by targeting HTML elements with certain classes, and extracts their text content. 
The scraped data is then used to create an instance of the Recipe class, which includes the recipe name, description, and the URL of the webpage. 
