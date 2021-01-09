# Morning

## Projects
#### Membership card
- Probably the quickest one for me to get an MVP out on, which will reduce stress of completion and allow me more time for improvements
- I can incorporate my own interests for this with the current specifications (i.e. it doesn't say what the membership card is for :) )
- The required date to be stored in the backend is clear

### Requirements
##### MVP:
- Users can sign up with an email :heavy_check_mark:
- Users can create a card on membership creation (i.e. on signing up) :heavy_check_mark:
- A user can see their card :heavy_check_mark:
- Users will not see other people's cards :heavy_check_mark:
- Basic sign in using username or email :heavy_check_mark:
- A user's card is persisted in the database :heavy_check_mark:
- Their card details include their name, and how many loyalty points they have :heavy_check_mark:

##### Additions:
- Test front end components :hourglass_flowing_sand:
- Password is hashed for storage in db :hourglass_flowing_sand:
- Users are only authorised to see their own card :hourglass_flowing_sand:
- Incorporate front-end storage? (e.g. Redux) :hourglass_flowing_sand:
- Users can sign up with email/username and password :heavy_check_mark:
- Styling :heavy_check_mark:
- Card details shows how long user has been a member for :heavy_check_mark:
- Card details shows if they are eligible for a discount
- Users can save discount codes to their account
- A page that shows what achievements/discounts you can get for the number of points
- Users can change their details
- A online store to "collect" points?

## Choice of Tech Stack
#### Frontend: Reactjs
- A popular framework with a large community, lots of documentation and support
- Using a framework applies a project structure, which speeds up the inital set up
- The style of the framework focuses on reusable components, which is optimal for designing a system for cards, which will adopt the the same base style for all customers
- Maintained by Facebook, who have plenty of resources and a responsibility to keep the framework up-to-date for their large community of users

#### Backend: Expressjs and Nodejs
- Another framework, quick set up that is tried and tested in the community
- Simple routing, and written with the intention of supporting the creation of REST APIs
- Abstracts a lot of node complexity, minimalises HTTP requests and responses
- Lots of well-supported libraries available to support building APIs and storing data

#### Database: MongoDB
- Quick set up
- Well-supported for web apps, used by large organisations such as Adobe and Facebook
- Database design is non-SQL, easy to design
- MongoDB is specifically designed to store JSONs, which is the object that is sent in requests of a REST API

##

- Combined these form the well known MERN stack, so there are plenty of project examples for me to draw inspiration from and makes it well discussed in the community - this will make it easier to find the right suggestions when troubleshooting too
- MERN is a fast an easy tech stack to set up, which makes it suitable for building web apps and has been tried and tested will a number of open source and organisation-based apps
- Since this is a small app, it's gonna be a full-stack mono-repo

