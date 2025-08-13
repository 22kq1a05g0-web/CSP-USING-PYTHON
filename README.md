n = 6

# Initialize the factorial variable to 1
fact = 1

# Calculate the factorial using a for loop
for i in range(1, n + 1):
    fact *= i

print(fact)
OUTPUT:<img width="1920" height="1080" alt="Screenshot (63)" src="https://github.com/user-attachments/assets/0f36d022-3e52-4af8-87f8-b5257f28827e" />

# Python program to determine whether
# the number is Armstrong number or not
def power(x, y):
    
    if y == 0:
        return 1
    if y % 2 == 0:
        return power(x, y // 2) * power(x, y // 2)
        
    return x * power(x, y // 2) * power(x, y // 2)

# Function to calculate order of the number
def order(x):

    # Variable to store of the number
    n = 0
    while (x != 0):
        n = n + 1
        x = x // 10
        
    return n

# Function to check whether the given 
# number is Armstrong number or not
def isArmstrong(x):
    
    n = order(x)
    temp = x
    sum1 = 0
    
    while (temp != 0):
        r = temp % 10
        sum1 = sum1 + power(r, n)
        temp = temp // 10

    # If condition satisfies
    return (sum1 == x)

# Driver code
x = 153
print(isArmstrong(x))

x = 1253
print(isArmstrong(x))

OUTPUT: <img width="1920" height="1080" alt="Screenshot (64)" src="https://github.com/user-attachments/assets/a6baa310-a8bb-4e17-9653-7535859dee0f" />
