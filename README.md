# CISprocjectspring2025
#Good try
#info for name
while True:
    name = input('What is your name: ')
    if name.isalpha():
        break
    else:
        input("Enter a valid name: ")

#info for age
while True:
    age = input('How old are you: ')
    if age.isdigit():
        break
    else:
        input("Enter a valid age: ")
#info for student ID
while True:
    ID = input('What is your student ID: ')
    if ID.isdigit() and 6 < len(ID) < 8:
        break
    else:
        input("There was an error please Try again: ")
#info for Phone number
while True:
    phone = input('What is your phone number: ')
    if phone.isdigit() and 9 < len(phone) < 11:
        break
    else:
        input("Invalid phone number")       

info.infol(name, age, ID, phone)
info.read_info(name, age, ID, phone)
print('Your info has been submitted and you will recieve an email shortly with an update')
