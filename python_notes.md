
*Keywords*
1. lambda operator or lambda function is used for creating small, one-time and anonymous function objects in Python. lambda operator can have any number of arguments, but it can have only one expression. It cannot contain any statements and it returns a function object which can be assigned to any variable.

2. A finally clause is always executed before leaving the try statement, whether an exception has occurred or not. When an exception has occurred in the try clause and has not been handled by an except clause (or it has occurred in an except or else clause), it is re-raised after the finally clause has been executed. The finally clause is also executed “on the way out” when any other clause of the try statement is left via a break, continue or return statement.

3. assert : This function is used for debugging purposes. Usually used to check the correctness of code. If a statement evaluated to true, nothing happens, but when it is false, “AssertionError” is raised . One can also print a message with the error, separated by a comma.

4. del : del is used to delete a reference to an object. Any variable or list value can be deleted using del.

5. raise : Also used for exception handling to explicitly raise exceptions. If no expressions are present, raise re-raises the last expression that was raised in the current scope.

6. pass : It is the null statement in python. Nothing happens when this is encountered. This is used to prevent indentation errors and used as a placeholder
  		'''
		\# Python program to test map, filter and lambda

		\# Function to test map 
		def cube(x):
			return x**2

		\# Driver to test above function

		\# Program for working of map 
		print "MAP EXAMPLES"
		cubes = map(cube, range(10))
		print cubes

		print "LAMBDA EXAMPLES"

		\# first parentheses contains a lambda form, that is 
		\# a squaring function and second parentheses represents
		\# calling lambda
		print (lambda x: x**2)(5)

		\# Make function of two arguments that return their product
		print (lambda x, y: x*y)(3, 4)


		print "FILTER EXAMPLE"
		special_cubes = filter(lambda x: x > 9 and x < 60, cubes)
		print special_cubes

		*output*
		MAP EXAMPLES
		[0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
		LAMBDA EXAMPLES
		25
		12
		FILTER EXAMPLE
		[16, 25, 36, 49]
		'''
7. Return sends a specified value back to its caller whereas *Yield* can produce a sequence of values. 
8. with

		'''
		with A() as a, B() as b:
			suite

		*is equivalent to*

		with A() as a:
			with B() as b:
				suite
		'''
	
9. is

		'''
		\# using is to check object identity
		\# string is immutable( cannot be changed once alloted)
		\# hence occupy same memory location
		print (' ' is ' ')

		\# using is to check object identity
		\# dictionary is mutable( can be changed once alloted)
		\# hence occupy different memory location
		print ({} is {})

		*output*
		True
		False	
		'''
10. non-local : This keyword works similar to the global, but rather than global, this keyword declares a variable to point to variable of outside enclosing function, in case of nested functions.






