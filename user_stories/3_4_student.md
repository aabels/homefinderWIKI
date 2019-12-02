# 3 - Student

## Student (Searching)

The following stories define how a Student will search for a place to live. The following assumes the user is logged in and authenticated with the service.

The following performance criteria applies to all requirements listed in this section:
* Searcher getting results after any initial search:
    * First paint < 1 s
    * First meaningful paint < 1.25s
    * Time to interactive < 1.5s
* Searcher getting refined results after applying a filter:
    * First paint < 0.5s
    * First meaningful paint < 1s
    * time to interactive < 1.25s

|No.|Statement|Acceptance Criteria|MVP|
|----|----|----|----|
|3.1|As a student, when I search for a place to live I want the search to consider the roommate questionnaire I completed so I can find a roommate I can get along with|When the user performs any search for a place, results show how good a match the poster is for them <ul><li>Each result visually indicates how good a match the poster is for them</li></ul>|Yes|
|3.2|As a student, I want to be able to search for a place to live based on location so I can see listings near where I want to live|The user is able to search by location / neighbourhood by typing in an address <ul><li>The user should be able to input a validated location</li><li>The range of the location search should be adjustable</li><li>Listings displayed should be visually near the inputted/adjusted location</li><li>Generate message about widening range if there are no listings available</li></ul>|Yes|
|3.3|As a student, I want to be able to search for a place to live based on the ameneties available so that I can see listings of places with those ameneties|The user can filter search results based on amenities. <ul><li>Filters for ameneties are available to click on near the search</li><li>Listings change according to filters toggled</li><li>The listings showed visually indicate they have the toggled ameneties available</li><li>If no listings are available with the filters applied, show a message about reducing search filtering</li></ul>|Yes|
|3.4|As a student, I should be able to search for a place to live based on property details|The user should be able to property details like # of bedrooms, unit size, rent price, etc. so I can find a place with qualities that I prefer. <ul><li>Filters based on property details should be displayed near the search</li><li>Listings should change based on toggled property details</li><li>Listings displayed should visually indicate similarity with specified property details</li><li>If no listings are available, show a message to widen search</li></ul>|Yes|
|3.5|As a student, I want to be able to search for a place to live based on a few qualities that I want my potential roommate to have so I can find a roommate I'd prefer.|The user is able to select filters regarding the poster of a listing <ul><li>The user should be able to toggle roommate filters</li><li>Results should change based on the toggles</li><li>Displayed listings should visually indicate the magnitude the poster is a match for the user</li><li>Better match roommates (more like qualities) should be displayed first</li><li>Listings should still show if there is no "good" match</li></ul>|No|
|3.6|As a student, I want to be able to search for a place to live based on the place's "house rules" (No parties, no overnight guests, etc.) so that I can find a place that I feel comfortable in.|The user can filter by house rules <ul><li>Filters for house rules should be available to toggle</li><li>Listings should change based on matching house rules</li><li>Better match places (more similar house rules) should be displayed first</li><li>Listings should still show if there is no "good" match</li></ul>|Yes|
|3.7|As a student, I want to be able to contact the person who made the listing so I can talk to them about moving into the listed property.| Preconditions: <ul><li>User is looking at a listing that they have found</li></ul> The user is able to click the contact poster button. After they have clicked the button the system should display the public contact information of the poster.|Yes | 



## 4: Student (Posting)

The following stories define how a Student will create and manage a posting.

The following performance criteria applies to all stories listed in this section:
* Loading the "My Listings" page
    * First paint < 1s
    * First meaningful paint < 1.25s
    * Time to interactive < 1.5s
* Submitting a posting/Editing a posting
    * Posting shows up in searches < 2s
* Deleting a posting:
    * Removes from "My Listings" and searches in < 1s

|No.|Statement|Acceptance Criteria|MVP|
|----|----|----|----|
|4.1| As a student, I want to be able to post a place that I am subletting so that other students seeking places can see mine| The student is able to post a place that they are subletting and will be displayed to possible matches based on the criteria given. <ul><li>Able to input a location</li><li>Able to specify the amenities available at the place by clicking icons</li><li>Able to specify rent price</li><li>Able input a description</li><li>Able to specify lease length</li><li>The poster's roommate preferences should be visually displayed</li><li>The "Cancel" button should always be clickable</li><li>Clicking "X" will return the poster back to the "My Listings" page</li><li>The listing should be viewable under "My Listings" (4.2)</li></ul>| Yes |
|4.1.1| As a student, I want to have a validation of my input on the posting page| The student is able to post a place that they are subletting and will be displayed to possible matches based on the criteria given. <ul><li>Validate the input</li><li>Submit button should be greyed out unless mandatory fields (location, rent price, amenities, and lease length) are filled out</li></ul>| No |
|4.1.2| As a student, I want to have go back to "My listings" by clicking "X".|<ul><li>Clicking "X" will return the poster back to the "My Listings" page</li><li>The listing should be viewable under "My Listings" (4.2)</li></ul>| Yes |
|4.2| As a student, I want to be able to see a list of postings that I have made so I can manage them| The student is able to see a list of postings that they have made <ul><li>Postings are ordered by recency</li><li>Option edit postings are visible</li></ul>| Yes|
|4.3 (Deprecated)| As a student, I want to see the possible matches for roommates on a subletting posting I have made so I gauge the interest of my posting| The student is able to select a posting that they have made and see a list of roommates that match their preferences. <ul><li>A list of potential roommates ordered by highest compatibility is visible</li><li>The user is able to click on the matching users an see the match's public contact information.</li></ul> | No, will not be done. The person searching for the posting will be the person to initiate contact. |
|4.4 | As a student, I want to be able to edit the preferences I have set for an individual posting I have made so I can clarify or fix any mistakes | The student is able to select a posting they have made and make changes to the preferences they have made <ul><li>The "Save" button is greyed out unless all mandatory fields are appropriately filled</li><li>Saving the edited posting navigates back to the "My Listings"</li><li>The edited posting appears in "My Listings"</li><li>The "Cancel" button is always clickable</li><li>Clicking "Cancel" navigates to the "My Listings" page</li><li>Navigating away from the edit page opens a dialog with a "You forgot to save" message</li></ul> | Yes|
|4.5|As a student, I should be able to delete a posting so that it can be removed from the website since I no longer want the posting up|The user is able to delete the posting from the "My Listings" page <ul><li>The "Delete" button is visible in the detailed edit posting page</li><li>Clicking "Delete" will show a dialog with a confirmation message.</li><li>Clicking "Cancel" or "Delete" will navigate back to the "My Listings" page</li><li>The deleted listing is no longer visible in "My Listings" or searches</li></ul>|Yes|
