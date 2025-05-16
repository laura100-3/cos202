                 Key components of the system:
The inventory management system is structured using Object-Oriented Programming (OOP) principles, featuring a clear hierarchy of classes that represent users and items within the system.
User Classes
1.	User Class: This is an abstract base class that defines common attributes and methods for all user types. It includes properties such as username and name, along with an abstract method getRole() that must be implemented by derived classes.
2.	Admin Class: Inherits from the User class and represents an administrator. The Admin class has methods to add and remove items from the inventory. When an admin adds or removes items, the system outputs a confirmation message indicating the action taken.
3.	Accountant Class: Also inherits from the User class, the Accountant class is responsible for generating inventory reports. It has a method that prints a summary of the current inventory, providing insights into stock levels.
4.	Cashier Class: This class represents a cashier who can process sales. The Cashier class includes a method to sell items, which checks the inventory for sufficient stock before completing the sale. If the sale is successful, a confirmation message is displayed; otherwise, an error message is shown.
Item Classes
1.	Item Class: This is another abstract base class that defines common attributes for all item types, such as name and pricePerUnit. It includes an abstract method getCategory() that must be implemented by subclasses.
2.	FreshProduce Class: Inherits from the Item class and represents perishable items. It includes an expiration date and a method to check if the item is expired. The class overrides the toString() method to provide detailed information about the item, including its expiration status.
3.	Provision Class: This class represents non-perishable items and inherits from the Item class. It does not have additional attributes beyond those defined in the base Item class.
4.	Electronics Class: Inherits from the Item class and includes additional attributes such as warranty years. It overrides the toString() method to include warranty information in its output.
Inventory Class
The Inventory class manages the collection of items and their quantities. It uses a HashMap to store items, where the key is the item name, and the value is an object that contains the item and its quantity. The Inventory class provides methods to add items, remove items, and print a summary of the current inventory.
Demonstration
The system includes a main class, InventoryManagementSystem, which serves as the entry point for the application. In the main method, instances of Admin, Accountant, and Cashier are created, along with various items such as Fresh Produce, Provision, and Electronics.
•	The Admin adds items to the inventory and can remove them as needed.
•	The Accountant generates a report that summarizes the current inventory status.
•	The Cashier processes sales, checking for sufficient stock before completing transactions.
The system outputs messages to the console to inform users of actions taken, such as successful additions, removals, and sales, as well as any errors encountered.
Overall, the design of the inventory management system is modular and extensible, allowing for easy updates and enhancements in the future.
