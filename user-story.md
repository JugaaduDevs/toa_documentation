# User story

### As a regular user of the app
- Register with name, email, phone and password <b>POST /user</b>
- Login with email and password <b>POST /authenticate </b>
- Update my profile 
    - Add a profile picture.
    - Add an address
- Browse through the menu items
    - Menu items are categorized as starter, main course, desert, drinks etc
    - Menu items have name of the item, description and an image 
    - Menu items have an associated price.
- Browse offer of the day
- Add 1 or more items to the cart
    - Add instructions per item like no garlic, how spicy ?
- View and edit items on the cart
    - View cart
    - Update quantity of a certain item in the cart
    - Remove an item from the cart.
- View price of the order.
- Price is updated when any change to cart is made including adding, removing of an item or updating the quantity of an item.
- Checkout the cart
    - Order is placed and message is displayed with the time of delivery.
    
    
### As an admin/worker user:

- User created using some background process (no registration provided)
- Login using the created credentials
- Update an item in the menu
    - Update the price
    - Update the description
    - Update the name
    - Upload a new image
- Delete an item from the menu
- Accept/Reject orders.
- Update delivery time for an order
- Add food item of the day/specials in the menu.
- Update the order status.


# Main entities and REST API specs
## 1. User

## 2. Address

## 3. Menu

## 5. Order