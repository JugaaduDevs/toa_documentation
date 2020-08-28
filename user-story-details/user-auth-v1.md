# User Registration and login

Below story describes the flow of the user's journey for:

1. Registration
2. Login/Sign in
3. Password Rest
4. Logout

## Registration
On the main screen of the app, if user elects to sign up, below steps are followed:

1. Signup form is presented below details:
	- Name
	- Email
	- Password
	- Confirm Password

2. When the details are filled and use clicks the sign up button, 
	
	1. Registration request is sent to the server.
	2. Server validates the incoming fields

		| Field    	| Optional/Mandatory 	| Min Length 	| Max Length 	|
		|----------	|--------------------	|------------	|------------	|
		|   Name   	|          M         	|      6     	|     30     	|
		|   Email  	|          M         	|      6     	|     30     	|
		| Password 	|          M         	|      8     	|    1024    	|
		| Phone	    |          M            |      0        |    15         |

	3. Server checks if the email is duplicate. If so, registration shoud fail
	4. Server encrypts the password
	5. Server stores the new user in the the database as inactive
	6. Server returns the newly saved user back to client

3. User sends an email to the user
	1. Email should contain a welcome message
	2. First timer offer
	3. URL with a token 

4. When the user clicks the URL, a server endpoint is called to activate the user.

*** Now the user can login to the app using the email and password. ***

<hr />

## Login/Sign in

On the first visit to the app, if the user elects to sign in

1. Login form is displayed with below
	- Email
	- Password
	- Login button

2. After user fills in the details and clicks the Login button, client calls the user.
3. Server, upon receiveing the request:
	1. Validates that the provided email is present in the database
	2. If not, login failure is returned (401 - Unauthorized)
	3. If yes, password is validated against stored password in the database
	4. If validation fails, failure is returned (401-Unauthorized)
	5. If password validates, a new JWT token is generated that contains
		- User ID: to identify the user
		- Expiration: 1 hour
	6. JWT token is returned back as Authorization header.

4. Username and password can be stored in the app for future login's.

*** Upon receiving the JWT token, client can call the next api's using the token. This is considered as login successful. ***

<hr />

## Forgot Password

If user selects the forgot password option, 

1. User is prompted to enter his/her email address.
2. When the email address is submitted to server
	1. Server validates if the email address is present in the database
	2. If not, failures response is returned back
	3. If yes, a new password is auto generated and stored in the database with an expiraton of 1 hour
	4. This password is sent to user's registered mail address.
	5. User can login with the given password.
3. If the user is validated against a generated password, server should indicate that to the client and client should be redirected to password reset page.
4. If user does not reset the password in 1 hour, the whole process has to be repeated.

<hr />

## Logout

The user does not logout. JWT expiration defines whether the user is able to access priviledged resources or not.

<br />

**NOTE:**

1. *Registration and forgot password is not applicable for Admin user since those users are created in the background*
2. *Role based authentication is based on JWT token*



















