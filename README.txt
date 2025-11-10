Pizza Generator

Outline your pseudocode in this document, as well as your explanation of the
function and a description of how you would update the code for varying prices. 

Also list any issues you experienced, other people you may have worked
with, or any other information that seems relevant about this assignment.

-------------------------------------------------------------------------------



PSEUDOCODE
---------------


FUNCTIONS:
----------
FUNCTION getRandomItems (Array: STRING, X: NUMBER)
    FOREACH item in the array
	ASSIGN random number
    ENDFOR
    SORT array items numerically by their random numbers
    MAP the names of the randomly sorted items onto Shuffled Array
    RETURN the first X items of Shuffled Array as STRINGS
ENDFUNCTION

FUNCTION pizzaCost (Size: STRING, Meats: NUMBER, Vegetables: NUMBER)
    RETURN (price of Size) + (Meats * (price of meat)) + (Vegetables * (price of vegetable))
ENDFUNCTION

FUNCTION orderPizza (Crust: NUMBER, Sauce: NUMBER, Cheese: NUMBER, Meats: NUMBER, Vegetables: NUMBER, Size: STRING)
    OBJECT
	PROPERTY crust: 
	    INPUT crusts list, Crust number
	    result = getRandomItems(crusts list, Crust number)
	    OUTPUT result
	PROPERTY sauce: 
	    INPUT sauces list, Sauce number
	    result = getRandomItems(sauces list, Sauce number)
	    OUTPUT result
	PROPERTY cheese: 
	    INPUT cheeses list, Cheese number
	    result = getRandomItems(cheeses list, Cheese number)
	    OUTPUT result
	PROPERTY meats: 
	    INPUT meats list, Meats number
	    result = getRandomItems(meats list, Meats number)
	    OUTPUT result
	PROPERTY vegetables: 
	    INPUT vegetables list, Vegetables number
	    result = getRandomItems(vegetables list, Vegetables number)
	    OUTPUT result
	PROPERTY size: Size
	PROPERTY price:  
	    INPUT Size, Meats number, Vegetables number
	    result = pizzaCost(Size, Meats number, Vegetables number)
	    OUTPUT result
    ENDOBJECT
RETURN OBJECT
ENDFUNCTION

FUNCTION yourTotalIs (pizzaOne: STRING, pizzaTwo: STRING, pizzaThree: STRING)
    RETURN (pizzaOne price) + (pizzaTwo price) + (pizzaThree price)
ENDFUNCTION


OBJECTS: 
----------
OBJECT pizza
    PROPERTY crust: Array
    PROPERTY sauce: Array
    PROPERTY cheese: Array
    PROPERTY meats: Array
    PROPERTY vegetables: Array
    PROPERTY sizePrice: Array
	PROPERTY small: 10
	PROPERTY medium: 15
	PROPERTY large: 20
    PROPERTY toppingPrices: Array
	PROPERTY meats: number
	PROPERTY vegetables: number
ENDOBJECT

OBJECT pizzaOne
    INPUT 1, 1, 1, 2, 3, small
    result = orderPizza(1, 1, 1, 1, 2, 3, "small")
    OUTPUT result
ENDOBJECT
PRINT pizzaOne

OBJECT pizzaTwo
    INPUT 1, 1, 2, 1, 4, medium
    result = orderPizza(1, 1, 2, 1, 4, "medium")
    OUTPUT result
ENDOBJECT
PRINT pizzaTwo

BJECT pizzaThree
    INPUT 1, 1, 1, 4, 2, large
    result = orderPizza(1, 1, 1, 4, 2, "large")
    OUTPUT result
ENDOBJECT
PRINT pizzaThree

INPUT pizzaOne, pizzaTwo, pizzaThree
result = yourTotalIs(pizzaOne, pizzaTwo, pizzaThree)
OUTPUT result
PRINT "Your total is: $" + result



ADJUSTMENTS FOR PREMIUM PRICES
---------------
OBJECT pizza with PREMIUM PRICES
    PROPERTY crust: Array
    PROPERTY sauce: Array
    PROPERTY cheese: Array
    PROPERTY meats: Array
	PROPERTY ham: 2.00
	PROPERTY sausage: 2.00
	PROPERTY chicken: 2.50
	PROPERTY pepperoni: 2.00
	PROPERTY bacon: 2.50
	PROPERTY ground beef: 2.50
    PROPERTY vegetables: Array
	PROPERTY basil: 1.50
	PROPERTY mushrooms: 1.50
	PROPERTY corn: 2.00
	PROPERTY pineapple: 2.00
	PROPERTY black olives: 2.00
	PROPERTY green peppers: 1.50
	PROPERTY red peppers: 1.50
	PROPERTY tomatoes: 1.50
	PROPERTY onions: 1.50
    PROPERTY sizePrice: Array
	PROPERTY small: 10
	PROPERTY medium: 15
	PROPERTY large: 20
ENDOBJECT

FUNCTION premiumPizzaCost (Size: STRING, Meats: STRING/ARRAY, Vegetables: STRING/ARRAY)
    FOREACH meat AND vegetable
	GET price
	ADD price to toppings cost
    ENDFOR
    RETURN (price of Size) + (toppings cost)
ENDFUNCTION

FUNCTION orderPremiumPizza (Crust: NUMBER, Sauce: NUMBER, Cheese: NUMBER, Meats: NUMBER, Vegetables: NUMBER, Size: STRING)
    OBJECT
	PROPERTY crust: 
	    INPUT crusts list, Crust number
	    result = getRandomItems(crusts list, Crust number)
	    OUTPUT result
	PROPERTY sauce: 
	    INPUT sauces list, Sauce number
	    result = getRandomItems(sauces list, Sauce number)
	    OUTPUT result
	PROPERTY cheese: 
	    INPUT cheeses list, Cheese number
	    result = getRandomItems(cheeses list, Cheese number)
	    OUTPUT result
	PROPERTY meats: 
	    INPUT meats list, Meats number
	    result = getRandomItems(meats list, Meats number)
	    OUTPUT result
	PROPERTY vegetables: 
	    INPUT vegetables list, Vegetables number
	    result = getRandomItems(vegetables list, Vegetables number)
	    OUTPUT result
	PROPERTY size: Size
	PROPERTY price:  
	    INPUT Size, meats names, vegetables names
	    result = pizzaCost(Size, meats names, vegetables names)
	    OUTPUT result
    ENDOBJECT
RETURN OBJECT
ENDFUNCTION

OTHER RESOURCES USED
---------------
Format for defining and calling functions in pseudo: https://pseudocode.deepjain.com/guides/functions/

Format for objects in pseudo: https://cs.stackexchange.com/questions/159604/declaring-a-javascript-object-in-pseudocode
