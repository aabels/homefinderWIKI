# Homefinder

Home Finder (Rent Whiz) Docs

<img src="static/img/logo.png" width=140, height=169/>

## Table of Contents

<!-- Do not extra whitespace the elements in the list pls -->
* [Overview](https://github.com/cmput401-fall2018/homefinder/wiki/Overview)
* [List of Preferences, Amenities, and Property Details](https://github.com/cmput401-fall2018/homefinder/wiki/List-of-Preferences,-Amenities,-and-Property-Details)
* [UI Navigation Diagram](https://xd.adobe.com/view/0933753a-e9a1-4888-8e35-a0ec8cf3a241-5c60/)
* High-level Design
  * [UML](https://github.com/cmput401-fall2018/homefinder/wiki/UML)
  * [API Doc](https://cmput401-fall2018.github.io/homefinder/)
  * [Architecture](https://github.com/cmput401-fall2018/homefinder/wiki/Architecture)
* [Technical Resources](https://github.com/cmput401-fall2018/homefinder/wiki/Technical-Resources)
* [Release Plan](https://github.com/cmput401-fall2018/homefinder/wiki/Release-Plan)
  * [Gantt Chart](https://docs.google.com/spreadsheets/d/1dqoMWZdIwfqNAUAb7G3nEjtsGyYaHCNr7KwcDuBeB2A/edit?usp=sharing)
* [Meeting Minutes](https://github.com/cmput401-fall2018/homefinder/wiki/Meeting-Minutes)
* [User Stories](https://github.com/cmput401-fall2018/homefinder/wiki/User-Stories)
  * [New User](https://github.com/cmput401-fall2018/homefinder/wiki/1_new_user)
  * [Returning User](https://github.com/cmput401-fall2018/homefinder/wiki/2_returning_user)
  * [Student](https://github.com/cmput401-fall2018/homefinder/wiki/3_4_student)
  * [Landlord](https://github.com/cmput401-fall2018/homefinder/wiki/5_landlord)
* React Set up
  * [Windows](https://github.com/cmput401-fall2018/homefinder/wiki/Setting-Up-React-(Windows))

## Brief Description

Home Finder is an enhanced home rental website specifically with roommate-matching feature. It mainly targets on university students who want to rent or sublet rooms.

## Project Description

The goal is to build a responsive website that allows post-secondary students to more reliably and accurately find roommates and accommodation in a quick and user friendly fashion. Most options today do not offer students an easy and reliable way to search for roommates and accommodation depending on their circumstances, academic goals, preferences, personality, culture, demographic or necessities. This responsive website aims to provide a one stop easy to use interface that will deliver this service to students in a quick, reliable, accurate and user friendly way. We are currently using a Facebook group for this purposes, but due to limitations in filtering, sorting, matching and overall management of listings, our users are left with a long list of postings in Facebook which they have to scroll through manually in the hope that they find the most suitable and relevant match.

### The main business outcomes are as follows

* Offer students the flexibility to specify and locate properties where they would like to live.
* Offer students the flexibility to select like-minded, suitable and vetted roommates who are also students.
* Provide a notification system to alert students whenever a match meeting their search criteria has been added, or when a match (roommate or landlord) would like to contact them.
* Move our existing user base from our Facebook group to the responsive website and use this as their primary source for finding accommodation, roommates and tenants. This is why it’s important users should be able to sign in with their Facebook profile.

## Glossary

|Term|Definition|
|---|---|
|RentWhiz / Home Finder|For the duration of this project, the two terms will be used interchangeably. RentWhiz is the _official_ name for the service.|
|User|Can be a student or landlord. General term for people using the site|
|[Student](https://github.com/cmput401-fall2018/homefinder/wiki/3_4_student)|Any student currently enrolled at a post-secondary institution|
|[Landlord](https://github.com/cmput401-fall2018/homefinder/wiki/5_landlord)|Any person who has managed a place for rent|
|[Tenant](https://github.com/cmput401-fall2018/homefinder/wiki/3_4_student)|Can be interchanged with student. Used to represent a student who is currently renting|
|[Property Details](https://github.com/cmput401-fall2018/homefinder/wiki/List-of-Preferences,-Amenities,-and-Property-Details#property-details)|Quantitative descriptions of property for rent.|
|[Preferences](https://github.com/cmput401-fall2018/homefinder/wiki/List-of-Preferences,-Amenities,-and-Property-Details#preferences)|Students personal (wants/needs) to be become a tenant.|
|[Amenities](https://github.com/cmput401-fall2018/homefinder/wiki/List-of-Preferences,-Amenities,-and-Property-Details#amenities)|Pleasant and comforting items that increase value of property for rent.|
|Must|For must-have features (dissatisfiers)|
|Should|For should-have features (satisfiers)|
|Can|For nice-to-have features (delighters)|

## Stakeholders

* Primary Users
  * Student renter
  * Roommate finder
  * Landlord
* Secondary Users
  * Administrator's
* Tertiary Users
  * TBD

## List of Similar Products
The following websites all providing rental services:
* [Kijiji](https://www.kijiji.ca/)
  * Kijiji allows both individual landlord and rental company to post their rental advertisements. People can contact them through email and phone number if they want to rent the place.
  * The type of the rental place can be varied from a shared room to the whole house.
  * It has a powerful search engine to satisfy different people's requests. 
  * It mainly targets on individual landlord and generic potential tenants. 
* [RentFaster](https://www.rentfaster.ca/)
  * RentFaster allows both individual landlord and rental company to post their rental advertisements. People can contact them through email and phone number if they want to rent the place.
  * The main type of the rental place is an apartment. Only a few are shared rooms.
  * It has a powerful search engine to satisfy different people's requests. 
  * It mainly targets on rental companies who want to rent out apartments and generic potential tenants. 
* [4Rent](https://4rent.ca/)
  * 4Rent allows rental company to post their rental advertisements with some cost. People can contact them through the website if they want to rent the place.
  * The main type of the rental place is an apartment. There is no shared room because of the cost of posting an advertisement.
  * It has a powerful search engine to satisfy different people's requests. 
  * It mainly targets on rental companies who want to rent out apartments and generic potential tenants. 
* [Renting Spaces](https://www.rentingspaces.ca/index.htm)
  * Renting Spaces allows both individual landlord and rental company to post their rental advertisements. People can contact them through email and phone number if they want to rent the place.
  * The main types of the rental place are shared room and apartment.
  * It has a special search engine which can search around a school. 
  * It mainly targets on individual landlords who want to rent out their rooms and student tenants. 
* [AirBNB](https://www.airbnb.ca/)
  * AirBNB provides hotel booking similar service. People who want to use their rooms to provide hotel service can post advertisement on this website. People can book a room similar as booking a hotel on this website.
  * The main type of rental place is shared room. 
  * It has a powerful search engine to satisfy different people's requests. 
  * It mainly targets on tourists who want to pay less for their hotel and landlords who have rooms to rent out. 
* [KoalaRoomie](https://koalaroomie.com/) 
  * KoalaRoomie allows individuals post their room rental advertisements, and people can post their requests and introduction as tenants, who are called roomies. People can contact landlords through the website if they want to rent the place.
  * The only type of the rental place is shared room.
  * It can only search rooms or roomies by price and location. 
  * It mainly targets on individual landlords who want to rent out their rooms and people who want to find a shared room in New York City. 

## Why Home Finder?
* We help individual people to post or find shared room on our website.
* We provide a roommate-matching feature, which let you find your desired roommate. You can find your roommate based on academic goals, personality, culture, etc. 
* We provide a powerful search engine to meet your requirements. You can search your desired living place or desired roommates.
* We target on post secondary students in Canada and landlords who want to rent out their rooms.
