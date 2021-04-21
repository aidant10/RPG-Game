# RPG-Game
# Island Survival
# This game will be survival based, you and a few other characters will attempt to get off the island your stranded on by finding your way to the plane that brought you there.
# Click the run button to begin the game.

# Title of 1st Dictionary (Characters)
print("In game characters:")

# Information for each character (Age, Where from, Description)
information = {
  'Martin Young': {
    'Age': 42,
    'From': 'West Valley, UT, US',
    'Description': 'Martin is the leader, strong and brave, father of Leo.',
  },

  'Leo Young': {
    'Age': 15,
    'From': 'West Valley, UT, US',
    'Description': 'Leo is very smart, extremely shy, son of Martin.',
  },

  'Jen Tai': {
    'Age': 31,
    'From': 'Toronto, ON, Canada',
    'Description': 'Jen is smart when it comes to food, Jen is a great cook.',
  },

  'Kasandra Gordan': {
    'Age': 25,
    'From': 'Bensalem, PA, US',
    'Description': 'Kasandra is good with technology,and friendly.',
  },

  'Peter Sutherland': {
    'Age': 63,
    'From': 'Regina, SK, Canada',
    'Description': 'Peter loves the outdoors, helpful with directions.'
  }
}

# For loop prints out each character profile
for person, person_info in information.items():
    print(f"\nName: {person}")
# Variables for values
    age = person_info['Age']
    country_from = person_info['From']
    description = person_info['Description']

# Print statements for the information
    print(f"\tAge: {age}")
    print(f"\tFrom: {country_from}")
    print(f"\tDescription: {description}")
    print("")


# Start of 2nd
print("Locations in game:")
print("")

# Second Dictionary (Locations)
locations = {
    'The Cave': ['Where the adventure begins.'],
    'The Jungle': ['Where obstacles are encountered.', 'Main location.'],
    'The Beach': ['Where plane is located.', 'Final destination.'],
}

# Printing all the locations and their info
for name, details in locations.items():
    print(f"{name} is: ")
    for detail in details:
        print(f"\t{detail}")
print("")


# Third Dictionary (items)
print("Available items in game:")
print("")

items = {
  'Knife': ['Martins trusty pocket knife he takes everywhere.'],
  'Rope': ['Found in the Jungle, very useful.'],
  'Compass': ['Used for a sense of direction.'],
  'Spear': ['Constructed by Martin, used as a defence mechanism.'],
  'First-aid kit': ['Incase of injury, always be prepared.']
}

# Prints out all the items and there uses
for item_name, item_info in items.items():
    print(f"{item_name} is: \n\t{item_info} ")

# Starts game
main_menu = "WELCOME TO THE ISLAND SURVIVAL\n"
main_menu += "Type 'start' to start the game.\n"

intro = input(main_menu)
if intro == 'start':
    print(f"You have started the game!\n")
else:
    print("\nInvalid Entry.\n")
print("")

# User picks where to begin journey
print("You've woken up on a beach what will you do?")
location = "Where would you like to explore? Cave, Beach or Jungle. \n"
location += "\nEnter 'quit' to end the game.\n\n"
print("")

# Executes the statements for each picked action
while True:
    message = input(location)
    if message == 'Cave':
        print(f"Your headed to the {message}!\n")
    elif message == 'Beach':
        print(f"Your headed to the {message}!\n")
    elif message == 'Jungle':
        print(f"Your headed to the {message}!\n")
    elif message == 'quit':
        break  # Ends game
    else:
        print("\nInvalid Entry.\n")
print("")

# Course: CS 30
# Period: 1
# Date created: 04/19/2021
# Date last modified: 04/19/2021
# Name: Aidan Tiller
# Description: RPG Continuous Gameplay

import inventory

# Beggining of map
from tabulate import tabulate

# Starts game
main_menu = "WELCOME TO THE ISLAND SURVIVAL\n"
main_menu += "Type 'start' to start the game.\n"
print("This game will be survival based, you and other          characters will attempt to get off the island.")
print("You will need to work your way from the cave, through the jungle then to the beach where your escape plane waits.\n")

intro = input(main_menu)
if intro == 'start':
    print(f"You have started the game!\n")
else:
    print("\nInvalid Entry.\n")
print("")

# Creation of the map
# Intro to map
print("Here is the map of the island!\n")


def print_map():
    """Creates a grid for the map using tabulate and arrays"""
    # Layout of map
    map = [[", 'Cave', "],
           ['Jungle', 'Quicksand', 'Beach'],
           [", 'Plane', "]]
    # Print map
    print(tabulate(map, tablefmt='grid'))

print("")

print_map()

# User picks where to begin journey
print("You've woken up in a cave what will you do?")
location = "Where would you like to explore? Cave, Beach or Jungle. \n"
location += "\nEnter 'quit' to end the game.\n\n"
print("")

# Executes the statements for each picked action
while True:
    message = input(location)
    if message == 'Cave':
        print(f"Your headed to the {message}!\n")
    elif message == 'Beach':
        print(f"Your headed to the {message}!\n")
    elif message == 'Jungle':
        print(f"Your headed to the {message}!\n")
    elif message == 'quit':
        break  # Ends game
    else:
        print("\nInvalid Entry.\n")
print("")
