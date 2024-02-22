# validator
#Checking for the presence of a period in the URL address https://www.python.org/
#Декораторы функций/Function decorators
import webbrowser
def validator(func):
    def wrapper(url):
        if "." in url:
            func(url)
        else:
            print("Неверный URL/Invalid URL")
    return wrapper
@validator
def open_url (url):
    webbrowser.open(url)

open_url("http://www.python.org")
