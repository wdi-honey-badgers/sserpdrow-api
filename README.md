# Sserpdrow Client
"Divine." - Vogue
"Watch this startup!" - Forbes
"eh." - Wordpress

Our app, Sserpdrow, is a Content Management System for businesses looking to add a blog and custom web pages to their online presence. Visitors of the company's websites can read the blogs and web pages, and Users (aka, the companies), can create, read, update, and delete blog posts and web pages.

## Tools:
* Scrum
* HTML
* CSS3
* Bootstrap
* Handlebars
* Javascript
* JQuery
* AJAX
* Node
* Curl
* MongoDB
* Mongoose
* Express
* Git
* Github
* Heroku

## Links:
Client Deployed: https://wdi-honey-badgers.github.io/sserpdrow-client/
Client Repo: https://github.com/wdi-honey-badgers/sserpdrow-api
API Deployed: https://honey-badgers-sserpdrow-api.herokuapp.com/
API Repo:  https://github.com/wdi-honey-badgers/sserpdrow-api

## User stories:
Visitors
As a visitor I want to GET a list of ALL the companies (ALL).
As a visitor I want to GET a navbar of ALL web pages for an individual company (SOME).
As a visitor I want to GET individual web pages (ONE).
As a visitor I want to GET a list of ALL blog posts of an individual company (SOME).
As a visitor I want to GET individual blog posts (ONE).

Users - Auth
As a user I want to sign up, login, change password, and sign out.
As a user I want to belong to a company (abstract entity, static).
As a user I want to have access to the dashboard view of my company when I login, granting me access to CRUD web pages belonging to my company, and CRUD blog posts belonging to my company and myself.

Users - Web pages (company ownership matters).
As a user I want to INDEX all web pages belonging to my company (displayed in a sidebar).
As a user I want to READ (open for editable view) individual web pages belonging to my company (by selecting them in the Index side-bar).
As a user I want to UPDATE existing web pages belonging to my company; title and content required.
As a user I want to CREATE new web pages for my company; title and content required.
As a user I want to DESTROY existing web pages belonging to my company.

Users - Blogs (individual user ownership matters)
As a user I want to INDEX all blog posts belonging to my company and authored by me (displayed in a sidebar).
As a user I want to READ (open for editable view) individual blog posts belonging to my company and authored by me (by selecting them in the Index side-bar).
As a user I want to UPDATE existing blog posts belonging to my company and authored by me; title and content required.
As a user I want to CREATE new blog posts for my company, authored by me; title and content required.
As a user I want to DESTROY existing blog posts for my company, authored by me.

## ERD:
https://imgur.com/UoREGv6

## Wireframes:
https://imgur.com/ut4CfyV

## Catalog of Routes
* ### Index
  - #### Request
    - ##### Verb
      - GET
    - ##### url
      -https://honey-badgers-sserpdrow-api.herokuapp.com/posts
    - ##### Body
      - n/a
  - #### Response
    - ##### Status
      - 200, OK
    - ##### Body
      ```
      {posts: [
          "post": {
            "title": "'"${TITLE}"'",
            "blog": "'"${BLOG}"'",
            "content": "'"${CONTENT}"'"
          }]
      }
      ```
      - The response body will be a posts object that contains an array of all of the different posts. There will be other attributes such as date and owner associated with each post.
* ### Show
  - ##### Verb
    - GET
  - ##### url
    -https://honey-badgers-sserpdrow-api.herokuapp.com/posts/:id
  - ##### Body
    - n/a
  - #### Response
  - ##### Status
    - 200, OK
  - ##### Body
    ```
    {
      "post": {
        "title": "'"${TITLE}"'",
        "blog": "'"${BLOG}"'",
        "content": "'"${CONTENT}"'"
      }
    }
    ```
    - The response body will be a post object. There will be other attributes such as date and owner associated with each post.
* ### Create
  - #### Request
    - ##### Verb
      -POST
    - ##### url
      -https://honey-badgers-sserpdrow-api.herokuapp.com/posts
    - ##### Body
    ```
    --request POST \
    --header "Content-Type: application/json" \
    --header "Authorization: Bearer ${TOKEN}" \
    --data '{
      "post": {
        "title": "'"${TITLE}"'",
        "blog": "'"${BLOG}"'",
        "content": "'"${CONTENT}"'"
          }
        }'
    ```
  - #### Response
    - ##### Status
      - 201, Created
    - ##### Body
    ```
    {
      "post": {
        "title": "'"${TITLE}"'",
        "blog": "'"${BLOG}"'",
        "content": "'"${CONTENT}"'"
      }
    }
    ```
* ### Update
  - #### Request
    - ##### Verb
      - PATCH
    - ##### url
      -https://honey-badgers-sserpdrow-api.herokuapp.com/posts/:id
    - ##### Body
      ```
      --request PATCH \
      --header "Content-Type: application/json" \
      --header "Authorization: Bearer ${TOKEN}" \
      --data '{
        "post": {
          "title": "'"${TITLE}"'",
          "blog": "'"${BLOG}"'",
          "content": "'"${CONTENT}"'"
          }
        }'
      ```
  - #### Response
    - ##### Status
      - 204, No Content
    - ##### Body
      - n/a
* ### Destroy
  - #### Request
    - ##### Verb
      - DELETE
    - ##### url
      -https://honey-badgers-sserpdrow-api.herokuapp.com/posts/:id
    - ##### Body
      ```
      --include \
      --request DELETE \
      --header "Authorization: Bearer ${TOKEN}"
      ```
  - #### Response
    - ##### Status
      - 204, No Content
    - ##### Body
      - n/a

## List of unsolved problems
  Future iterations of the appliocation will be enhanced in the following ways:
    * Websites and blogs will be more uniquely different
      - the resource for posts will be split into a blog and Website resource
      - Websites will have more rich content than Blogs
    * Websites and blogs will be grouped by user/company
    * Each company will have admins that can publish and delete posts while normal users can edit and save drafts
    * Clicking on a post will show an expanded view of the post

## Story about development planning/obstacles:
Captains log, Star date 201807171632.
Raining. Dreary. Our voyage began in class room 6. We first created Wireframes, ERD's, User Stories, and a Scrum board. Had a 3 on 1 with Mike - He recommended we actually shrink our ERD to combine Users with Companies (make them the same entity). And the Earth fell below as we spread our wings in flight. Our "Posts" resource (which doubles as web pages and Blog posts for the time being) was created by Dan, our user Authentication was created by Catherine, merged and deployed all of these things, connected to the front end client side view, and tested their functionality via curl scripts and HTML forms.
- The Honey Badger Sean

Captain's log, supplemntal.
Sunny and pleasant today, we continued coding along in classroom 6. We encountered the Merge Conflict today and together we strategized to defeat them. We also discovered a few bugs, like the impressive-sounding Unprocessable Entity, but we have dealt with them before, so they didn't stall us for long. We are now able to successfully create, show, update, and delete posts. A user can only update and delete their own posts, as is appropriate. We dug into styling today, utilizing CSS, Bootstrap, and Handlebars. Tomorrow we embark on the final day of this mission.
- Honey Badger Catherine

Stargate Log:
Planet P2X-3YZ was amazing. Fantastic internet connections on the plannet for writing the code for our Sserpdrow application. Day was primarilly spent improving user interactions with the application and styling. Now there is a confirmation dialog when a user wishes to delete a resource that he created. Additionally, the update and delete buttons do not show unless a user is signed in. When signed in, the buttons are only visible on the resources that that user has created. Team executed well today. We tackled difficult problems and pairing really helped get through the major hurdles and it also kept us focused on the mission.
- Honey Badger Captiain Dan
