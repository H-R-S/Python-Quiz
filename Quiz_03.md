## [Quiz: 03](https://github.com/H-R-S/Python-Quiz/blob/main/Quiz_03.md)

Q1. Traffic Jam Predictor: Write a Python program that predicts the likelihood of a traffic jam on a given road in Karachi. Ask the user to input the time of day (in 24- hour format) and the expected weather conditions (sunny, cloudy, or rainy). Use if-else statements to check the time and weather conditions, and store the result in a boolean variable called traffic_jam. Display a message to the user indicating whether or not a traffic jam is likely.
### Code:
```
time_of_day = input("Enter the time of day (in 24-hour format) ex.(14:30): ")
weather_conditions = input("Enter the expected weather conditions (sunny, cloudy, or rainy): ")
traffic_jam = False

hour=int(time_of_day[:2])
min=int(time_of_day[3:])

if (hour >= 7 and hour <= 10) or (hour >= 16 and hour <= 19):
    if weather_conditions == "rainy":
        traffic_jam = True
    elif weather_conditions == "cloudy":
        traffic_jam = False
    else:
        traffic_jam = False
else:
    traffic_jam = False

if traffic_jam:
    print("Traffic jam")
else:
    print("No Traffic Jam")
    
```
### Output:
```
Enter the time of day (in 24-hour format) ex.(14:30): 11:23
Enter the expected weather conditions (sunny, cloudy, or rainy): sunny
No Traffic Jam

```

Q2. Movie Ticket Prices: Write a Python program that calculates the price of a movie ticket in Karachi. Ask the user to input their age and the day of the week (Monday to Sunday). Use if-else statements to check the age and day, and calculate the ticket price accordingly. Store the result in a variable called ticket_price and display it to the user
### Code:
```
age = int(input("Enter your age: "))
day = input("Enter the day of the week (monday to sunday): ")
weekend = ["saturday", "sunday"]
weekdays = ["monday", "tuesday", "wednesday", "thursday", "friday"]

ticket_price = 0
is_allowed = True

if age < 18:
  if day in weekdays:
    is_allowed = False
  elif day in weekend:
    ticket_price = 100
elif age >= 18 and age <= 65:
    if day in weekdays:
        ticket_price = 250
    elif day in weekend:
        ticket_price = 350
else:
    ticket_price = 200


if is_allowed:
  print("The ticket price is Rs. " + str(ticket_price) + "/-")
else:
  print("Sorry, you are not allowed today")

```
### Output:
```
Enter your age: 10
Enter the day of the week (monday to sunday): tuesday
Sorry, you are not allowed today

```

Q3. Pizza Delivery: Write a Python program that calculates the delivery time for a pizza in Karachi. Ask the user to input the distance to the delivery address (in kilometers) and the time of day (in 24-hour format). Use if-else statements to check the distance and time, and calculate the estimated delivery time accordingly. Store the result in a variable called delivery_time and display it to the user.
### Code:
```
distance = float(input("Enter the distance to the delivery address (in kilometers): "))
time_of_day = input("Enter the time of Order (in 24-hour format) ex.(14:30): ")

hour = int(time_of_day[:2])
min = int(time_of_day[3:])

if distance <= 3:
    delivery_time = min + 10
elif distance <= 6:
    delivery_time = min + 20
else:
    delivery_time = min + 30

print(f"Estimated delivery time: {hour}:{delivery_time}")

```
### Output:
```
Enter the distance to the delivery address (in kilometers): 23
Enter the time of Order (in 24-hour format) ex.(14:30): 12:01
Estimated delivery time: 12:31

```

Q4. Cricket Match Result: Write a Python program that predicts the winner of a cricket match in Karachi. Ask the user to input the team names and their recent form (win, loss, or draw). Use if-else statements to check the recent form of each team, and store the result in a boolean variable called team1_wins. Display a message to the user indicating which team is likely to win.
### Code:
```
team1 = input("Enter team 1 name: ")
team1_form = input("Enter team 1 recent form (win, loss, or draw): ")
team2 = input("Enter team 2 name: ")
team2_form = input("Enter team 2 recent form (win, loss, or draw): ")

if team1_form == "win" and team2_form != "win":
    team1_wins = True
elif team2_form == "win" and team1_form != "win":
    team1_wins = False
else:
    team1_wins = None

if team1_wins is None:
    print("Draw")
elif team1_wins:
    print(f"{team1} win the match in Karachi.")
else:
    print(f"{team2} win the match in Karachi.")

```
### Output:
```
Enter team 1 name: IU
Enter team 1 recent form (win, loss, or draw): win
Enter team 2 name: IBA
Enter team 2 recent form (win, loss, or draw): draw
IU win the match in Karachi.

```

Q5. Restaurant Rating: Write a Python program that calculates the rating of a restaurant in Karachi based on the user's feedback. Ask the user to rate the food quality, service, and atmosphere on a scale of 1 to 10. Use if-else statements to check the ratings and calculate the overall rating accordingly. Store the result in a variable called restaurant_rating and display it to the user.
### Code:
```
food_quality = int(input("Rate the food quality (out of 10): "))
service = int(input("Rate the service (out of 10): "))
atmosphere = int(input("Rate the atmosphere (out of 10): "))

if (food_quality >= 1) and (food_quality <= 10) and (service >= 1) and (service <= 10) and (atmosphere >= 1) and (atmosphere <= 10):
    restaurant_rating = (food_quality + service + atmosphere) / 3
    print("The overall rating of the restaurant is: ", restaurant_rating)
else:
    print("Please rate on a scale of 1 to 10.")
    
```
### Output:
```
Rate the food quality (out of 10): 22
Rate the service (out of 10): 12
Rate the atmosphere (out of 10): 1
Please rate on a scale of 1 to 10.

```

Q6. Traffic Violation Checker: Write a Python program that checks if a driver in Karachi has violated any traffic laws. Ask the user to input their license plate number and the type of violation (speeding, running a red light, etc.). Use if-else statements to check the license plate number and violation type, and store the result in a boolean variable called violation_found. Display a message to the user indicating whether or not a violation was found.
### Code:
```
violation_data = {
    "ABC-1234": ["speeding", "wrong parking"],
    "DEF-9012": ["speeding", "wrong way"],
    "GHI-3456": ["wrong parking", "break signal"],
    "JKL-7890": ["wrong parking", "wrong way"],
    "MNO-5678": ["wrong parking", "break signal"]
}

license_plate = input("Enter your license plate number: ")
violation_type = input("Enter the type of violation: ")

if license_plate in violation_data:
    if violation_type in violation_data[license_plate]:
        violation_found = True
    else:
        violation_found = False
else:
    violation_found = False

if violation_found:
    print("Violation found for license plate", license_plate)
else:
    print("No violation found for license plate", license_plate)

```
### Output:
```
Enter your license plate number: mno
Enter the type of violation: speeding
No violation found for license plate mno

```

Q7. School Grading System: Write a program that takes in a student's name, grade, and percentage in their exam. If the percentage is between 90% and 100%, give the student an "A" grade. If it's between 80% and 89%, give them a "B" grade. If it's between 70% and 79%, give them a "C" grade. If it's between 60% and 69%, give them a "D" grade. If it's below 60%, give them an "F" grade. Use boolean variables to track whether the student passed or failed.
### Code:
```
name = input("Enter student's name: ")
grade = input("Enter student's grade: ")
percentage = float(input("Enter exam percentage: "))

grade_letter = 'None'
passed = False

if percentage >= 90 and percentage <= 100:
    grade_letter = 'A'
elif percentage >= 80 and percentage <= 89:
    grade_letter = 'B'
elif percentage >= 70 and percentage <= 79:
    grade_letter = 'C'
elif percentage >= 60 and percentage <= 69:
    grade_letter = 'D'
else:
    grade_letter = 'F'

if grade_letter == 'F':
    passed = False
else:
    passed = True

print("\nName:", name)
print("Grade:", grade)
print("Percentage:", percentage)
print("Grade Letter:", grade_letter)
print("Passed:", passed)

```
### Output:
```
Enter student's name: Haris
Enter student's grade: A
Enter exam percentage: 91

Name: Haris
Grade: A
Percentage: 91.0
Grade Letter: A
Passed: True

```

Q8. Cricket Score Tracker: Write a program that takes in the current score and the number of overs played in a cricket match. If the current score is below 50 runs, display a message indicating that the team needs to pick up the pace. If the score is between 50 and 100 runs, display a message indicating that the team is doing okay. If the score is above 100 runs, display a message indicating that the team is doing well. Use boolean variables to track whether the team is winning or losing the match.
### Code:
```
score = int(input("Enter current score: "))
overs = int(input("Enter number of overs played: "))

run_rate = score / overs

message = ''
winning = False

if score < 50:
    message = "The team needs to pick up the pace."
    winning = False
elif score >= 50 and score <= 100:
    message = "The team is doing okay."
    winning = False
else:
    message = "The team is doing well."
    winning = True

print("Current score:", score)
print("Current run rate:", run_rate)
print("Message:", message)
print("Winning:", winning)

```
### Output:
```
Enter current score: 101
Enter number of overs played:  12
Current score: 101
Current run rate: 8.416666666666666
Message: The team is doing well.
Winning: True

```

Q9. Traffic Signal Simulator: Write a program that simulates a traffic signal at an intersection. Use boolean variables to represent the current state of each traffic signal (red, yellow, or green). If the current signal is red, display a message indicating that cars must stop. If the current signal is yellow, display a message indicating that cars must prepare to stop. If the current signal is green, display a message indicating that cars may proceed.
### Code:
```
red = True
yellow = False
green = False

print("Signal is red. Cars must stop.")

import time
time.sleep(10)

red = False
yellow = True

print("Signal is yellow. Cars must prepare to stop.")

time.sleep(5)

yellow = False
green = True

print("Signal is green. Cars may proceed.")

```
### Output:
```
Signal is red. Cars must stop.
Signal is yellow. Cars must prepare to stop.
Signal is green. Cars may proceed.

```

Q10. Restaurant Bill Calculator: Write a program that calculates the bill at a restaurant. Ask the user to input the number of items they ordered, the name and price of each item, and the percentage of tax to be applied. Use if-else statements to check the tax percentage and calculate the final bill accordingly. Use boolean variables to track whether the customer left a tip or not.
### Code:
```
num_items = int(input("Enter the number of items you ordered: "))

subtotal = 0
tax_rate = 0
tip_amount = 0
tip_given = False

for i in range(num_items):
    name = input("Enter the name of item #" + str(i+1) + ": ")
    price = float(input("Enter the price of item #" + str(i+1) + ": "))
    subtotal += price

tax_percent = float(input("Enter the tax percentage: "))

if tax_percent == 0:
    tax_rate = 0
else:
    tax_rate = tax_percent / 100
tax_amount = subtotal * tax_rate

total_bill = subtotal + tax_amount

tip_response = input("Do you want to leave a tip? (yes or no) ")
if tip_response.lower() == "yes":
    tip_given = True
    tip_amount = total_bill * 0.1
    total_bill += tip_amount


print("Subtotal: $", subtotal)
print("Tax rate: ", tax_rate)
print("Tax amount: $", tax_amount)
print("Total bill: $", total_bill)
if tip_given:
    print("Tip amount: $", tip_amount)
else:
    print("No tip given.")

```
### Output:
```
[ ]
num_items = int(input("Enter the number of items you ordered: "))

subtotal = 0
tax_rate = 0
tip_amount = 0
tip_given = False

for i in range(num_items):
    name = input("Enter the name of item #" + str(i+1) + ": ")
    price = float(input("Enter the price of item #" + str(i+1) + ": "))
…print("Tax rate: ", tax_rate)
print("Tax amount: $", tax_amount)
print("Total bill: $", total_bill)
if tip_given:
    print("Tip amount: $", tip_amount)
else:
    print("No tip given.")

Enter the number of items you ordered: 3
Enter the name of item #1: burger
Enter the price of item #1: 900
Enter the name of item #2: fries
Enter the price of item #2: 350
Enter the name of item #3: drink
Enter the price of item #3: 100
Enter the tax percentage: 25
Do you want to leave a tip? (yes or no) yes
Subtotal: $ 1350.0
Tax rate:  0.25
Tax amount: $ 337.5
Total bill: $ 1856.25
Tip amount: $ 168.75

```

Q11. Shipping Fee Calculator: Write a program that calculates the shipping fee for a package based on its weight and destination. Ask the user to input the weight of the package and the name of the destination city. Use if-else statements to check the destination and calculate the shipping fee accordingly. Use boolean variables to track whether the package requires special handling or not.
### Code:
```
weight = float(input("Enter the weight of the package in kg: "))
destination = input("Enter the name of the destination city: ")

shipping_fee = 0
special_handling = False

if destination.lower() == "karachi":
    if weight <= 1:
        shipping_fee = 200
    elif weight <= 5:
        shipping_fee = 500
    elif weight <= 10:
        shipping_fee = 1000
    else:
        shipping_fee = 1500
elif destination.lower() == "lahore":
    if weight <= 1:
        shipping_fee = 250
    elif weight <= 5:
        shipping_fee = 600
    elif weight <= 10:
        shipping_fee = 1200
    else:
        shipping_fee = 1800
else:
    if weight <= 1:
        shipping_fee = 300
    elif weight <= 5:
        shipping_fee = 700
    elif weight <= 10:
        shipping_fee = 1400
    else:
        shipping_fee = 2000

if weight > 10:
    special_handling = True

print("Shipping fee: Rs.", shipping_fee)

if special_handling:
    print("Special handling required.")
else:
    print("No special handling required.")

```
### Output:
```
Enter the weight of the package in kg: 25
Enter the name of the destination city: karachi
Shipping fee: Rs. 1500
Special handling required.

```

Q12. Phone Number Validator: Write a program that checks whether a given phone number is valid or not. Ask the user to input a phone number in the format "+92 XXX-XXXXXXX". Use if-else statements to check whether the phone number is in the correct format and whether the area code is valid for Karachi. Use boolean variables to track whether the phone number is valid or not.
### Code:
```
phone_number = input("Enter a phone number in the format '+92 XXXX-XXXXXXX': ")

valid_format = False
valid_area_code = False
valid_number = False

if phone_number.startswith("+92 ") and "-" in phone_number:
    valid_format = True

area_code = phone_number[3:7]
valid_area_codes = ["030", "031", "032", "033"]
if area_code in valid_area_codes:
    valid_area_code = True

if valid_format and valid_area_code:
    number = phone_number[8:]
    if len(number) == 7 and number.isdigit():
        valid_number = True

if valid_format and valid_area_code and valid_number:
    print("Phone number is valid.")
else:
    print("Phone number is not valid.")

```
### Output:
```
Enter a phone number in the format '+92 XXXX-XXXXXXX': +92 0310-3337801
Phone number is not valid.

```
