# BedtimeNinja "Bedtime Stories for Kids"
## MVP specification for the BedtimeNinjas website:
* User registration and authentication: Users should be able to register for a new account and log in to access the website's features.
* Book browsing and selection: Users should be able to browse through a collection of children's books, filter them by age range and genre, and select books to add to their library.
* Book reading: Users should be able to read books directly on the website using a responsive e-reader that allows for easy navigation and comfortable reading.
* Audio playback: Users should be able to listen to audio versions of the books, with the option to play, pause, and skip chapters.
* User preferences: Users should be able to set preferences for the types of books they are interested in, such as age range, genre, and reading level.
* User history: Users should be able to view their reading and listening history, including the books they have read or listened to, and their progress.
* Responsive design: The website should be optimized for both desktop and mobile devices, with a user-friendly interface that adjusts to the screen size.
* Secure login: The website should implement secure login procedures, such as password hashing and SSL/TLS encryption.
* Content management: The website should have a content management system that allows administrators to add, remove, and update books and audio files.
* Basic analytics: The website should track basic analytics, such as user engagement and popular books, to help inform future development decisions.
* Blog section: The website should have a blog section for parents to access articles and tips on parenting, sleep routines, and bedtime stories.
* Social media channels: The website should include social media buttons linking to BedtimeNinjas' social media channels, such as Facebook, Twitter, and Instagram, to increase user engagement and drive traffic to the website.

This MVP specification provides a starting point for the BedtimeNinjas website, focusing on the core features that will provide value to users and enable them to comfortably enjoy bedtime stories. As the website grows and develops, additional features and functionality can be added to enhance the user experience.

## The architecture for the BedtimeNinjas website could consist of the following components:

1. Front-end: The user interface, built with HTML, CSS, and JavaScript, enables users to browse and interact with the website's features. The front-end communicates with the back-end API to fetch and display data.

2. Back-end API: The back-end API, built with Python and Flask, handles incoming requests from the front-end and retrieves data from the database. The API also provides authentication and authorization functionality to ensure that only authenticated users can access protected resources.

3. Database: The database, built with MySQL, stores all of the website's data, including user accounts, book metadata, and reading history.

4. Audio storage: The audio files for the books are stored in a separate location, such as an Amazon S3 bucket, and accessed through URLs stored in the database.

## Website Architecture Map:

![arc diagram](https://user-images.githubusercontent.com/72882307/226424173-0b466a2e-a9c3-434d-a01c-9c37888ddfa3.png)

## APIs and Methods
## API Routes for Bedtime Ninja Web Application:

/api/v1/stories
GET: Returns a list of all stories available in the database.
POST: Adds a new story to the database.
 
/api/v1/stories/{story_id}
GET: Returns details of a specific story identified by story_id.
 
/api/v1/categories
GET: Returns a list of all categories available in the database.
 
/api/v1/categories/{category_id}
GET: Returns details of a specific category identified by category_id.
 
/api/v1/users
GET: Returns a list of all users available in the database.
POST: Adds a new user to the database.
 
/api/v1/users/{user_id}
GET: Returns details of a specific user identified by user_id.
PUT: Updates the details of a specific user identified by user_id.
 
### API Endpoints or Function/Methods for other clients:
There will be an API endpoint to allow other clients to retrieve a list of all stories available in the database. This endpoint can be used to fetch data for external applications that may want to display bedtime stories on their own platform.
 
Endpoint: /api/v1/stories
Method: GET
Parameters: None
Response: Returns a JSON object containing an array of all stories available in the database, each story containing details such as title, description, author, and category.
 
There will also be an API endpoint to allow external clients to retrieve details of a specific story identified by story_id.
 
Endpoint: /api/v1/stories/{story_id}
Method: GET
Parameters: story_id (string)
Response: Returns a JSON object containing details of the story identified by story_id, including title, description, author, and category.
 
Another API endpoint that will be created for external clients is to allow them to retrieve a list of all categories available in the database.
 
Endpoint: /api/v1/categories
Method: GET
Parameters: None
Response: Returns a JSON object containing an array of all categories available in the database, each category containing details such as name and description.
 
### 3rd Party APIs:
Bedtime Ninja Web Application may use the following 3rd party APIs:
* Google AdSense API - to display ads on the website and generate income.
* Stripe API - to handle payment processing for any purchases made through the website.
* Amazon Polly API - to generate audio versions of bedtime stories for users who prefer listening to stories rather than reading them.

## User Stories:
* As a parent, I want to be able to listen to audible bedtime stories with my child so that I can give my voice a break while still providing them with the comfort of hearing a bedtime story.
* As a single parent, I struggle with putting my child to bed every night. With BedtimeNinja, I hope to find a variety of engaging and calming bedtime stories to help my child fall asleep quickly and easily.
* As a busy and stressed parent, I often find bedtime to be a source of anxiety and frustration when my child won't fall asleep. With BedtimeNinja, I hope to find a range of stories that can help soothe my child and make bedtime a more enjoyable experience for both of us.
* As a child, I want to be able to listen to stories with sound effects and music to make the experience more immersive and entertaining.
* As a child, I want to be able to earn rewards or points for listening to stories, so I feel motivated to participate and look forward to bedtime.


