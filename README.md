Exercise B2: Calculating Pi 

It is possible to get an estimate of the mathematical constant π by using a random process. The idea is based on the fact that the area of a circle of radius 1 is equal to π, and the area of a quarter of that circle is π/4. Here is a picture of a quarter of a circle of radius 1, inside a 1-by-1 square:



The area of the whole square is one, while the area of the part inside the circle is π/4. If we choose a point in the square at random, the probability that it is inside the circle is π/4. If we choose N points in the square at random, and if C of them are inside the circle, we expect the fraction C/N of points that fall inside the circle to be about π/4. That is, we expect 4*C/N to be close to π. If N is large, we can expect 4*C/N to be a good estimate for π, and as N gets larger and larger, the estimate is likely to improve.

We can pick a random point in the square by choosing numbers x and y in the range 0 to 1 (using random.random()). Since the equation of the circle is x*x+y*y=1, the point lies inside the circle if x*x+y*y is less than 1. One trial consists of picking x and y and testing whether x*x+y*y is less than 1. To get an estimate for π, you have to do many trials, count the trials, and count the number of trials in which x*x+y*y is less than 1,

For this exercise, you should write a program that does this computation and displays the result. The computation should be done in a separate thread, and the results should be displayed periodically. 
It should print the result on the console after running each batch of, say, one million trials. (printing the result after each trial doesn't make sense, since millions of trials can be done in one second, and trying to change the display millions of times per second would be inefficient)

Each print will show: Real value of Pi, Calculated value of Pi, and number of attempts.

Get the number of batches from the user, and run this amount of computation batches (remember each batch activates a million trials).


