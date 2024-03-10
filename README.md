# -to-Check-Prime-Number-or-not
 num = 11
# If given number is greater than 1
if num > 1:
	# Iterate from 2 to n / 2
	for i in range(2, int(num/2)+1):
		# If num is divisible by any number between
		# 2 and n / 2, it is not prime
		if (num % i) == 0:
			print(num, "is not a prime number")
			break
	else:
		print(num, "is a prime number")
else:
	print(num, "is not a prime number")
 # approach-2
 from math import sqrt
# n is the number to be check whether it is prime or not
n = 1

# this flag maintains status whether the n is prime or not
prime_flag = 0

if(n > 1):
	for i in range(2, int(sqrt(n)) + 1):
		if (n % i == 0):
			prime_flag = 1
			break
	if (prime_flag == 0):
		print("True")
	else:
		print("False")
else:
	print("False")
 # approach-3
 import math

def is_prime(n):
	if n < 2:
		return False
	i = 2
	while i*i <= n:
		if n % i == 0:
			return False
		i += 1
	return True

print(is_prime(11)) # True
print(is_prime(1)) # False


