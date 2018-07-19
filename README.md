# Sserpdrow Client
"Divine."
- Vogue
"Watch this startup!"
- Forbes
"eh."
- Wordpress
Our app, Sserpdrow, is a Content Management System for businesses looking to add a blog and custom web pages to their online presence. Visitors of the company's websites can read the blogs and web pages, and Users (aka, the companies), can create, read, update, and delete blog posts and web pages.

## Tools:
Scrum
HTML
CSS3
Bootstrap
Handlebars
Javascript
JQuery
AJAX
Node
Curl
MongoDB
Mongoose
Express
Git
Github
Heroku

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

## List of unsolved problems

## Story about development planning/obstacles:
Captains log, Star date 201807171632
Raining. Dreary. Our voyage began in class room 6. We first created Wireframes, ERD's, User Stories, and a Scrum board. Had a 1 on 1 with Mike - He recommended we actually shrink our ERD to combine Users with Companies (make them the same entity). And the Earth fell below as we spread our wings in flight. Our "Posts" resource (which doubles as web pages and Blog posts for the time being) was created by Dan, our user Authentication was created by Catherine, merged and deployed all of these things, connected to the front end client side view, and tested their functionality via curl scripts and HTML forms.
- The Honey Badger Sean
