# Goal:
The goal of this document is to give clear instrutions on testing the backend and front end of the homefinder project.

### New user integration testing:
#### Test 1: Signing in with Facebook
   Preconditions: User has a Facebook account. User is on the login page.
 1. User clicks the Facebook login button and authorizes the homefinder app
 2. User has to receive email verification email and go to link.
 
Expected outcome:
  * User is redirected to the landing page.
  * User authenticates.
  * User has a cookie named token saved to their browser.

#### Test 2: Signing in with Email & Password
  Preconditions: User has a validated account. User is on the login page.
 1. User inputs a correct username and password and clicks log in
 
Expected outcome:
  * User has a cookie named token
  * If there is an error with the fields the error will display under the input.

#### Test 3: User is able to sign up for an account:
 1. Navigate to the signup page
 2. Enter the information for a new user.
 3. Submit the new user.

 Expected outcome:
  * User should be redirected to the landing page and en email confirmation should be sent


#### Test 4: User is able to confirm email address:
 Preconditions: 
  * User has account made, and the confirmation email url

Steps:
 1. Navigate to the `frontend/api-auth/registration/account-confirm-email/token`
 2. User should see the confirm email button
 3. User click confirm

Expected Outcomes:
 * User is redirected to the homepage.

