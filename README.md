import random
import string

def generate_password(length=12):
  """Generate a secure random password with uppercase, lowercase, numbers, and special characters."""
  characters = string.ascii_letters + string.digits+ string.punctuation
  password = ''.join(random.choice(characters) for_in range(length))
  return password 

if __name__ == "__main__":
  try:
     length = int(input("Enter password length: "))
     if length < 4:
             print("Password length should be at least 4 characters.")
     else:
             password = generate_password(length)
             print(f"Generated Password: {password}")
  except ValueError:
        print("Please enter a valid number.")
