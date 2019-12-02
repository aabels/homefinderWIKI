# 5 - Landlord

The following stories define how a landlord will begin to interact with the system. Assuming the user has a verified log-in and is signed into the website.

The following performance criteria applies to specified requirements (#.) listed in this section:
* Clearing all applied Preferences to Listing (5.3):
    * First paint < 0.5s
    * First meaningful paint < 1s
    * time to interactive < 1s
* Property Listing Submission (5.4):
    * POST becomes visible to potential Students < 2s


|No.|Statement|Acceptance Criteria|MVP|
|----|----|----|----|
|5.1|As a Landlord/Sub-letter user, I want to answer questions about my property so I can create my property listing.|   The user will answer most of the questions and preview their property listing.<ul><li>Validate user exists (is Active)</li><li>Verification of Mandatory Question(s) answered.</li><li>Visual preview exists.</li></ul>|Yes|
|5.2|As a Landlord/Sub-letter user, I want to be able to change my answers to my property questionnaire, so I can fix a mistake a made.|The user will be able to "Go Back" and change their answers from the preview of the property listing.<ul><li>"Edit" Button -> re-directs to Questions (5.1) to edit</li><li>Save loaded changes to Questions</li><li>Allow Preview Validation</li></ul>|Yes|
|5.3|As a Landlord/Sub-letter user, I want to delete my "preview" property listing and start over since I answered incorrectly and changing my answers will take too long.|The user is able to clear/remove the property listing and start over.<ul><li>"Clear" Button -> affirmation prompt</li><li>Remove the Posting object</li><li>"create" posting prompt(5.1)</li></ul>|Yes|
|5.4|As a Landlord/Sub-letter user, I want to "approve" my preview property listing and POST, since all my changes have been made.|The user is able to POST their custom property listing on the site.<ul><li>"Confirm" Button -> "Are you sure" dialog </li><li>Return to Nav Page</li></ul>|Yes|