# Ordering

## Definitions:

**Order:** An order is represented in the database as below:

- ID (Generated by the database) - Need a better way
- List of order items
- Status of the order. Valid values are below
	- PENDING TO BE ACCEPTED
	- ACCEPTED BY THE RESTAURANT
	- BEING PREPARED
	- DISPATCHED
	- DELIVERED
- Customer info

**Order Items:** Order item is represented in the database as below:

- ID (Generated by the database)
- Reference to menu item
- Quantity



<hr>

## The cart

- A cart displays the items being bought. It contains:

	1. List of items
		1. Name
		2. Quantity
		2. Instructions
		3. Price
	2. Totals
		1. Total price calculated
		2. Tax info
	3. Flat discount information

- User should be able to remove items from the cart
- User should be able to update the quantity of an item from the cart
- Any change in quantity should update the total value
- Any item removed from cart should update the totals in the cart.

**NOTE:** The cart can only be accessed securely i.e. after login.

<hr>

## Order

Once user is satisfied with the selected items. He can choose to order or cancel the order entirely.

- Cancelling the order redirects the user to Categories view.
- Completing the order results into following action:
	- Client sends the order details to server
	- Server creates an order and corresponding order details
	- Order status is "PENDING TO BE ACCEPTED"


### Order status update

- Updates to the order are done from the backend.
- Status of the order is polled from the client using a REST call.




































