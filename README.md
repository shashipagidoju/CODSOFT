import random
import string

def generate_password(length):
  
    characters = string.ascii_letters + string.digits + string.punctuation
    

    password = ''.join(random.choices(characters, k=length))
    
    return password


if __name__ == "__main__":
    while True:
        try:
            length = int(input("Enter the length of the password: "))
            if length <= 0:
                print("Length should be greater than zero. Please enter a valid length.")
                continue
            else:
                break
        except ValueError:
            print("Invalid input. Please enter a valid integer length.")
    
    password = generate_password(length)
    print(f"Generated password: {password}")
