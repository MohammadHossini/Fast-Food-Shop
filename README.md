# Fast-Food-Shop
Fast Food Shop
Introduction
This project implements an online food purchase system from the restaurant. The system includes features such as registration, menu sorting, password hashing, and route finding between two locations.

Data items
This project uses two data files:

txt.Discount: contains a list of valid discount codes written in binary form.
txt.Menu: Contains a list of dishes with prices and waiting time for preparation. Each line of this file contains the information of a food as follows:
perl
Copy code
name, price, time to be ready
Spinach Salad - $7 - 4m
Margherita Pizza - $11 - 22m
Possible operations
1. Registration and login
The program first asks the user to sign up and then log in. The user's password is stored in a hashed form.

2. Show menu and order food
After entering, the food menu from the txt.Menu file will be shown to the user. The user can sort the menu by price (pyramid sorting) and order food. (The user can choose several dishes).

3. Use the discount code and choose to send by courier
After ordering food, the user can enter a discount code. If the discount code is valid, 10% discount will be deducted from the final amount. User can also choose to send by courier.

4. Show the courier route
After choosing to send by courier, the user enters the destination and the program shows the route of the courier to the destination.

Further Details
1. Password hashing
A method has been developed to hash the password by multiplying the position (index) of each character in its ASCII code and then subtracting that value. Example:

User password: AB25
hash = 65*1 - 1
hash = hash + 66*2 - 2
hash = hash + 50*3 - 3
hash = hash + 53*4 - 4
hash = 549

2. Sort by food price
Heap sort algorithm is used to sort the menu based on price.

3. Valid discount codes
Valid discount codes are located in the txt.Discount file, which is binary. By constructing a Huffman tree, these codes are converted into letters and a list of valid codes is created. If the user's discount code was in this list, 10% discount will be deducted from the final amount.

4. Graph modeling for the neighborhoods around the restaurant
The neighborhoods around the restaurant are modeled as a graph. The restaurant is located at node A and a route from the restaurant to the destination is displayed for the user.
