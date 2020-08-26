# User story

### As a customer of the app
- Register with name, email, phone and password <b>POST /user</b>
    - E-mail Verification .
    - Details Validations
- Login with email and password <b>POST /authenticate </b>
    - Forgot PWD .
- Update my profile 
    - Add a profile picture. (Optional)
    - Add an address
- Browse through the menu items
    - Menu items are categorized (eg - starter, main course, desert, drinks ) - Should be customizable by admins.
    - Menu items have name of the item, description , image and hotness level (mild,medium,hot) 
    - Menu items have an associated price.
- Browse offer of the day (Optional).
- Browse featured Items.
- Discounts 
    - Flat discounts - full Cart .
    - Discounts on first orders. 
- Add 1 or more items to the cart
    - Add Items from the main Menu screen with default spicyness level .
    - Click the Items to enter the instruction screen / layover .
        - Add instructions per item like no garlic. Some Items would not allow adding instructions .
        - Select Spicyness level.
- View and edit items on the cart
    - View cart
    - Update quantity of a certain item in the cart
    - Remove an item from the cart.
- View price of the order.
- Price is updated when any change to cart is made including adding, removing of an item or updating the quantity of an item.
- Checkout the cart
    - Order is placed and message is displayed with the time of delivery.
- Display order history.

- Optional 
    - Amend the order withing one minute .
    - Profile Picture.
    - Review Restaurant.
    - Re-order from the list.
        - Item Validation .
    
### As an admin/worker user:

- User created using some background process (no registration provided)
- Login using the created credentials
- Update an item in the menu
    - Update the price
    - Update the description
    - Update the name
    - Upload a new image (Optional)
- Delete an item from the menu
- Mark Not Available .
- Accept/Reject orders.
- Update delivery time for an order.
- Add food item of the day/specials in the menu. (Optional)
- Add and Update featured Items from existing list.
- Update the order status.
- Order Summary . 

- Optional 
    - Analytics .


# Main entities and REST API specs
## 1. User

## 2. Address

## 3. Menu

## 5. Order
