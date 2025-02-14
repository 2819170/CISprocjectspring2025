# CISprocjectspring2025
Good try
from pynput import keyboard
import info

from pynput import keyboard

def on_press(key):
    try:
        print('alphanumeric key {0} pressed'.format(
            key.char))
    except AttributeError:
        print('special key {0} pressed'.format(
            key))

def on_release(key):
    print('{0} released'.format(
        key))
    if key == keyboard.Key.esc:
        # Stop listener
        return False

# Collect events until released
with keyboard.Listener(
        on_press=on_press,
        on_release=on_release) as listener:
    listener.join()

# ...or, in a non-blocking fashion:
listener = keyboard.Listener(
    on_press=on_press,
    on_release=on_release)
listener.start()

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
