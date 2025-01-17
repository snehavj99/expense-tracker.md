# Define a class called ExpenseTracker
     class ExpenseTracker:
  # Initialize the class with an empty dictionary to store expenses
           def __init__(self):
                   self.expenses = {}

   # Method to add a new expense
    def add_expense(self, category, amount):
   # Check if the category already exists in the dictionary
        if category in self.expenses:
   # If it exists, add the new amount to the existing amount
            self.expenses[category] += amount
        else:
   # If it doesn't exist, create a new entry with the given amount
            self.expenses[category] = amount

  # Method to view all expenses
    def view_expenses(self):
   # Iterate over each category and amount in the dictionary
        for category, amount in self.expenses.items():
   # Print the category and amount
            print(f"{category}: RS:{amount}")

  # Method to calculate the total of all expenses
    def calculate_total(self):
   # Return the sum of all amounts in the dictionary
        return sum(self.expenses.values())

# Define the main function
    def main():
  # Create an instance of the ExpenseTracker class
    tracker = ExpenseTracker()
    
  # Run an infinite loop until the user chooses to exit
    while True:
  # Print the menu options
        print("1. Add Expense")
        print("2. View Expenses")
        print("3. Calculate Total")
        print("4. Exit")
        
  # Ask the user to choose an option
        choice = input("Choose an option: ")
        
   # Handle each option
        if choice == "1":
  # Ask for the category and amount, and add the expense
            category = input("Enter category: ")
            amount = float(input("Enter amount: "))
            tracker.add_expense(category, amount)
        elif choice == "2":
  # View all expenses
            tracker.view_expenses()
        elif choice == "3":
  # Calculate and print the total
            print(f"Total: RS:{tracker.calculate_total()}")
        elif choice == "4":
  # Exit the loop
            break
        else:
  # Handle invalid options
            print("Invalid choice. Please choose again.")

# Check if this script is being run directly (not imported)
    if __name__ == "__main__":
   # Call the main function
    main()



