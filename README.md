# Importing the necessary libraries
import random

# Defining the AI class
class AI:
    def __init__(self):
        self.greetings = ["Hello!", "Hi there!", "Greetings!"]
        self.goodbyes = ["Goodbye!", "See you later!", "Farewell!"]

    def greet(self):
        return random.choice(self.greetings)

    def say_goodbye(self):
        return random.choice(self.goodbyes)

    def generate_response(self, user_input):
        # Add your own logic for generating responses here
        response = "I'm sorry, but I don't understand."
        return response

# Creating an instance of the AI class
my_ai = AI()

# Greeting the user
print(my_ai.greet())

# Running the AI conversation loop
while True:
    # Getting user input
    user_input = input("User: ")

    # Checking for exit command
    if user_input.lower() == "exit":
        print(my_ai.say_goodbye())
        break

    # Generating AI response
    ai_response = my_ai.generate_response(user_input)
    print("AI:", ai_response)
