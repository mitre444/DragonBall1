# Dragon Ball API Project

This project is a simple Python program that connects to the [Dragon Ball API](https://dragonball-api.com/) to explore characters and planets.  
It allows the user to list characters, search by ID, search by name, and view details such as race, ki, and origin planet.
Note: This API does not require an API key, so no .env file was needed for this project.

## Features 
- List characters (with ID and name)
- View details of a character (race, ki, origin planet)
- View the planet’s name and description
- Search characters by name

## How to Run 
1. Make sure you have Python 3.12+ installed.
2. Install the required library:
pip install requests

# Issues 
## Issue 1: API returns inconsistent data structures 
Problem: When searching by name, sometimes the API returned a list and other times a dictionary with `"items"`. 
Solution: Added logic using `isinstance()` to handle both cases. 

## Issue 2: Program crashed when invalid ID was entered 
Problem: Entering a non-existent character ID caused the program to break. 
Solution: Implemented error handling to print `"Character not found."` instead of crashing. 

## Issue 3: No clear way to stop the program 
Problem: Once inside the menu, the user had no clean way to exit. 
Solution: Added a `while True` loop with a `"Do you want to continue? (y/n)"` prompt to let the user exit safely.

# Future Improvements 
- Add pagination to display more than 10 characters at a time.
- Add filtering by race or power level.
- Possibly create a simple UI instead of console-only. 
