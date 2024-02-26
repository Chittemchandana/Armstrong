# Armstrong
# Python program to check if the number is an Armstrong number or not
# Check Armstrong number (for 3 digits)
# take input from the user
num = int(input("Enter a number: "))

# initialize sum
sum = 0

# find the sum of the cube of each digit
temp = num
while temp > 0:
   digit = temp % 10
   sum += digit ** 3
   temp //= 10

# display the result
if num == sum:
   print(num,"is an Armstrong number")
else:
   print(num,"is not an Armstrong number")

# approach2
# Check Armstrong number of n digits
num = 1634

# Changed num variable to string, 
# and calculated the length (number of digits)
order = len(str(num))

# initialize sum
sum = 0

# find the sum of the cube of each digit
temp = num
while temp > 0:
   digit = temp % 10
   sum += digit ** order
   temp //= 10

# display the result
if num == sum:
   print(num,"is an Armstrong number")
else:
   print(num,"is not an Armstrong number")

# approach3
def is_armstrong(num):
	num_str = str(num)
	n = len(num_str)
	sum = 0
	for digit in num_str:
		sum += int(digit)**n
	if sum == num:
		return True
	else:
		return False
num=153
print(is_armstrong(num))


# approach4
import math

def isArmstrong(num):
	n = num
	numDigits = 0
	sum = 0
	
	# Find number of digits in num
	while n > 0:
		n //= 10
		numDigits += 1
	
	n = num
	
# Calculate sum of digits raised to the power of numDigits
	while n > 0:
		digit = n % 10
		sum += math.pow(digit, numDigits)
		n //= 10
	
# Check if num is Armstrong number or not
	if sum == num:
		return True
	return False

# Example 1
num1 = 1634
if isArmstrong(num1):
	print(num1, "is an Armstrong number.")
else:
	print(num1, "is not an Armstrong number.")

# Example 2
num2 = 120
if isArmstrong(num2):
	print(num2, "is an Armstrong number.")
else:
	print(num2, "is not an Armstrong number.")
