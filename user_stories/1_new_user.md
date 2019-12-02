# 1 - New User

These stories cover a new users first encounter with the service.

|No.|Statement|Acceptance Criteria|MVP|
|----|----|----|----|
|1.1|As a new user, when I visit the site for the first time I want to be provided with a landing page so I can choose what I want to do.|The user is presented with a landing page with options for a student/tenant, landlord, as well as a login/sign up button. <ul><li>When the user clicks on the create listing button they will be prompted to login.</li><li>When the user clicks on the search listings button they will be prompted to login.</li></ul> |Yes|
|1.2|As a new user, I want to be able to sign up with my Facebook account so I do not need to make an account|The user is able to login with their Facebook account Post conditions:<ul><li>User is able to search listings if they have a validated post secondary email without being prompted to login.</li><li>User is able to create a posting without being prompted to login</li></ul>|Yes|
|1.3|As a new user, I want to be able to signup with my email and password because I do not want to share my Facebook profile|The user is able to sign up using their email address and password.|Yes|
|1.4|As a new user with a validated post secondary email, I want to be prompted to fill in my roommate preferences so I can find possible roommates.| Precondition: <ul><li>User is logged in with a valid post secondary email</li></ul> User is prompted to fill in the roommate preferences questionnaire after they have been logged in for the first time. The user is able skip this and fill in the questionnaire at a later time. <br>Back End Requirements: <ul><li>Roommate preferences are stored in the database for the user.</li></ul>| Yes | 
|6.1|As a user, I want to have a email confirmation page after sign up.|Precondition: <ul><li>User has signed up with a valid post secondary email</li></ul> User will confirm their email address by clicking confirm button.|Yes|
