### Contact Book Application

#### Features:
1. **Add a New Contact**: Store a contact's name, phone number, and email address.
2. **View All Contacts**: Display all contacts in the contact book.
3. **Search for a Contact**: Search for a contact by name.
4. **Delete a Contact**: Delete a contact by name.
5. **Update a Contact**: Update the details of an existing contact.


#### Instructions:
1. Create a dictionary to store the contacts.
2. Implement functions for each feature.
3. Use a while loop to display a menu and handle user input.

Here's a simple implementation to get you started:

```python
def display_menu():
    print("\nContact Book Menu:")
    print("1. Add a New Contact")
    print("2. View All Contacts")
    print("3. Search for a Contact")
    print("4. Delete a Contact")
    print("5. Update a Contact")
    print("6. Exit")

def add_contact(contacts):

    

def view_contacts(contacts):

    

def search_contact(contacts):

    
    

def delete_contact(contacts):

    

def update_contact(contacts):

    

def main():
    contacts = {}
    while True:
        display_menu()
        choice = input("Choose an option (1-6): ")
        if choice == '1':
            add_contact(contacts)
        elif choice == '2':
            view_contacts(contacts)
        elif choice == '3':
            search_contact(contacts)
        elif choice == '4':
            delete_contact(contacts)
        elif choice == '5':
            update_contact(contacts)
        elif choice == '6':
            print("Exiting Contact Book.")
            break
        else:
            print("Invalid choice. Please try again.")

if __name__ == "__main__":
    main()
```

### Key Concepts Practiced:
- **Dictionaries**: To store contact information.
- **Functions**: To modularize the code and handle different operations.
- **Loops**: To keep the application running until the user decides to exit.
- **Conditionals**: To handle different user inputs.

You can extend this project with additional features like saving contacts to a file, loading contacts from a file, or adding error handling for invalid inputs.
