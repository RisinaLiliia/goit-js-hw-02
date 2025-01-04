# goit-js-hw-02

Task 1. Ordering droids

Perform this task in the task-1.js file

The repair droids sales station is ready to launch, all that remains is to write the software for the sales department. Declare the function makeTransaction(quantity, pricePerDroid, customerCredits), which composes and returns a message about the purchase of repair droids.

It declares three parameters, the values ​​of which will be set when it is called:

quantity — the number of droids ordered

pricePerDroid — the price of one droid

customerCredits — the amount of funds on the customer's account

Add the function as follows:

Declare a variable to store the total amount of the order (the total cost of all ordered droids) and assign it an expression for calculating this amount.
Add a check to see if the customer will be able to pay for the order:

if the amount to be paid exceeds the number of credits on the customer's account, the function should return the string "Insufficient funds!"
otherwise, the function should return the string "You ordered <quantity> droids worth <totalPrice> credits!", where <quantity> is the number of droids ordered, and <totalPrice> is their total cost.

Take the code below and insert it after the declaration of your function to verify that it works correctly. The results of its work will be displayed in the console.

console.log(makeTransaction(5, 3000, 23000)); // "You ordered 5 droids worth 15000 credits!"

console.log(makeTransaction(3, 1000, 15000)); // "You ordered 3 droids worth 3000 credits!"
console.log(makeTransaction(10, 5000, 8000)); // "Insufficient funds!"
console.log(makeTransaction(8, 2000, 10000)); // "Insufficient funds!"
console.log(makeTransaction(10, 500, 5000)); // "You ordered 10 droids worth 5000 credits!"

Leave this code for the mentor to check.

What the mentor will pay attention to when checking:

The declared function makeTransaction(quantity, pricePerDroid, customerCredits)
The call makeTransaction(5, 3000, 23000) returns "You ordered 5 droids worth 15000 credits!"
The call makeTransaction(3, 1000, 15000) returns "You ordered 3 droids worth 3000 credits!"
The call makeTransaction(10, 5000, 8000) returns "Insufficient funds!"
The call makeTransaction(8, 2000, 10000) returns "Insufficient funds!"
Calling makeTransaction(10, 500, 5000) returns "You ordered 10 droids worth 5000 credits!"

Task 2. Formatting a message

Perform this task in the task-2.js file

Declare a function formatMessage(message, maxLength), which takes a string (message parameter) and checks its length against the specified maximum length (maxLength parameter).

Complete the function code so that:

If the length of the string is equal to or less than maxLength, the function returns the original string unchanged.

If the length exceeds maxLength, the function truncates the string to maxLength characters, adds an ellipsis "..." at the end, and returns the truncated version.

Take the code below and paste it after the declaration of your function to verify that it works correctly. The results of its operation will be displayed in the console.

console.log(formatMessage("Curabitur ligula sapien", 16)); // "Curabitur ligula..."
console.log(formatMessage("Curabitur ligula sapien", 23)); // "Curabitur ligula sapien"
console.log(formatMessage("Vestibulum facilisis purus nec", 20)); // "Vestibulum facilisis..."
console.log(formatMessage("Vestibulum facilisis purus nec", 30)); // "Vestibulum facilisis purus nec"
console.log(formatMessage("Nunc sed turpis a felis in nunc fringilla", 15)); // "Nunc sed turpis..."
console.log(formatMessage("Nunc sed turpis a felis in nunc fringilla", 41)); // "Nunc sed turpis a felis in nunc fringilla"

Leave this code for a mentor to review.



What the mentor will pay attention to when checking:

The declared function formatMessage(message, maxLength)
The function call formatMessage("Curabitur ligula sapien", 16) returns "Curabitur ligula..."
The function call formatMessage("Curabitur ligula sapien", 23) returns "Curabitur ligula sapien"
The function call formatMessage("Vestibulum facilisis purus nec", 20) returns "Vestibulum facilisis..."
The function call formatMessage("Vestibulum facilisis purus nec", 30) returns "Vestibulum facilisis purus nec"
The function call formatMessage("Nunc sed turpis a felis in nunc fringilla", 15) returns "Nunc sed turpis..."
The function call formatMessage("Nunc sed turpis a felis in nunc fringilla", 41) returns "Nunc sed turpis a felis in nunc fringilla"

Task 3. Spam Check

Perform this task in the task-3.js file

The checkForSpam(message) function takes a string (message parameter), checks it for the prohibited words spam and sale, and returns the result of the check. The words in the message parameter string can be in any case, for example SPAM or sAlE.

Complete the function code so that:

If a prohibited word (spam or sale) is found, the function returns true
If there are no prohibited words in the string, the function returns false

Take the code below and insert it after the declaration of your function to check the correctness of its operation. The results of its operation will be displayed in the console.

console.log(checkForSpam("Latest technology news")); // false
console.log(checkForSpam("JavaScript weekly newsletter")); // false
console.log(checkForSpam("Get best sale offers now!")); // true
console.log(checkForSpam("Amazing SalE, only tonight!")); // true
console.log(checkForSpam("Trust me, this is not a spam message")); // true
console.log(checkForSpam("Get rid of sPaM emails. Our book in on sale!")); // true
console.log(checkForSpam("[SPAM] How to earn fast money?")); // true

Leave this code for the mentor to check.

What the mentor will pay attention to when checking:

The function checkForSpam(message) is declared.
Calling the function checkForSpam("Latest technology news") returns false
Calling the function checkForSpam("JavaScript weekly newsletter") returns false
Calling the function checkForSpam("Get best sale offers now!") returns true
Calling the function checkForSpam("Amazing SalE, only tonight!") returns true
Calling the function checkForSpam("Trust me, this is not a spam message") returns true
Calling the function checkForSpam("Get rid of sPaM emails. Our book in on sale!") returns true
Calling the function checkForSpam("[SPAM] How to earn fast money?") returns true

Task 4. Delivery of the goods

Perform this task in the file task-4.js

Declare the function getShippingCost(country), which should check the possibility of delivering the goods to the user's country (parameter country) and return a message about the result. Be sure to use the switch statement.

The format of the returned string is "Shipping to <country> will cost <price> credits", where instead of <country> and <price> you need to substitute the appropriate values.

List of countries and shipping costs:

China — 100 credits

Chile — 250 credits

Australia — 170 credits

Jamaica — 120 credits

The list shows that delivery is not possible everywhere. If the specified country is not in the list, then the function should return the string "Sorry, there is no delivery to your country".

Take the code below and insert it after the declaration of your function to check the correctness of its operation. The results of its operation will be displayed in the console.

console.log(getShippingCost("Australia")); // "Shipping to Australia will cost 170 credits"
console.log(getShippingCost("Germany")); // "Sorry, there is no delivery to your country"
console.log(getShippingCost("China")); // "Shipping to China will cost 100 credits"
console.log(getShippingCost("Chile")); // "Shipping to Chile will cost 250 credits"
console.log(getShippingCost("Jamaica")); // "Shipping to Jamaica will cost 120 credits"
console.log(getShippingCost("Sweden")); // "Sorry, there is no delivery to your country"

Leave this code for a mentor to review.



What the mentor will pay attention to when checking:

The function getShippingCost(country) is declared
The switch statement is used in the function body
The call getShippingCost("Australia") returns "Shipping to Australia will cost 170 credits"
The call getShippingCost("Germany") returns "Sorry, there is no delivery to your country"
The call getShippingCost("China") returns "Shipping to China will cost 100 credits"
The call getShippingCost("Chile") returns "Shipping to Chile will cost 250 credits"
The call getShippingCost("Jamaica") returns "Shipping to Jamaica will cost 120 credits"
The call getShippingCost("Sweden") returns "Sorry, there is no delivery to your country"
