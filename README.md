# Pharmaceutical-Company
Database for a pharmaceutical company that sells drugs to hospitals. 

Through the database a system that helps in the management and sales of these drugs will be designed. The system should be efficient in inventory management, and order processing.
Entities
1.	 Hospital
The system should store every hospital that orders and purchases the drugs that the pharmaceutical company is selling. It should include information about every hospital such as the name, address, contact information and each hospital should have a unique identifier.
2.	Drug
The database should store drug information which includes the name, description of the drug, dosage, expiry date and the cost. 
3.	Supplier
The database should make it possible for the business to manage its suppliers. Each supplier needs to have a name, a unique ID, their contact information, such as their phone number and email.
4.	Inventory
The database should make it possible for the business to control its inventory. A drug ID, and the supplier ID, and a quantity should be listed for each individual drug with a different supplier.
5.	Order
The database will allow the company to see all the orders they have to process. Each order will have a unique order ID, the date of the order. Each order is linked to a Hospital ID. 
6.	Order Detail
This stores the Order ID and the Drug ID and the quantity being ordered. This enables for multiple drugs to be ordered. An order can have multiple drugs and will take into consideration the amount of each drug ordered.
7.	Invoice
Every transaction should have an invoice generated by the system. Each invoice must be identified by a special invoice number, the date it was created, and the Order ID.


Entity Relationships
1.	Hospital: Order (one-to-many)
•	A hospital can place multiple orders, and each order is associated with one hospital.
2.	Drug: OrderDetail (one-to-many)
•	Each drug can be ordered by multiple hospitals, and each order can contain multiple drugs.
3.	Order: OrderDetail (one-to-many)
•	One order can have multiple order details, but each order detail can only be associated with one order.
4.	Supplier: Inventory (one-to-many)
•	A supplier can supply multiple items in the inventory, and each item in the inventory can only be supplied by one supplier.
5.	Drug: Inventory (one-to-many)
•	Each drug can have multiple instances in the inventory, but each instance of a drug in the inventory can only belong to one drug.
6.	Hospital: Invoice (one-to-many)
•	A hospital can receive multiple invoices, but each invoice is associated with only one hospital.
7.	Order: Invoice (one-to-one)
•	Each order is associated with one invoice, and each invoice is associated with only one order.
