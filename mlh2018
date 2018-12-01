import requests

print("Welcome to Chuck Norries jokes, please select from the following:\n"
	  "1:For random jokes\n"
	  "2:For joke categories\n"
	  "3: For exit")

user_input = 0
while user_input != 3:
	user_input = int(input())
	if user_input == 1:
		response = requests.get("https://api.chucknorris.io/jokes/random")
		data = response.json()
		print(data['value'])

	if user_input == 2:
		categories = requests.get("https://api.chucknorris.io/jokes/categories")
		data = categories.json()
		for element in data:
			print(element)
		category = input("Enter the category\n")
		joke = requests.get("https://api.chucknorris.io/jokes/random?category=%s" % category)
		data1 = joke.json()
		print(data1['value'])

	if user_input == 3:
		print("Bye! Enjoy your day\n")

	else:
		print("Please ener a valid input\n")

