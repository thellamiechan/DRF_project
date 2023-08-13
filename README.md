# DRF_project
She Codes DRF Module
Bookarina

by {{ Julie Powell }}
She Codes crowdfunding project - DRF Backend.
About

This crowdfunding site is for authors who wish to raise money to self publish their book. Self publishing is often the only recourse authors have in today's super competitve publishing era. Self publishing can be expensive, though. Crowdfunding to the rescue!

Features
The features your MVP will include. (Remember this is a working document, you can change these as you go!)
feature - clickable all-project page leading to individual projects and user pages
feature - pledge pages linked to both the project funding and the owner who posted it


Stretch Goals
{{ Outline three features that will be your stretch goals if you finish your MVP }}

Stretch goal- ability to delete a project (I know this should have been MVP, but honestly I didn't have time to get to it)
Stretch goal- pagination and the ability to determine how many items per page shown
Stretch goal- user portal, with incentives and rewards

API Specification

![API specification](APIspec.png)


Database Schema

{{ ![Schema for Database](<schema for database.png>) }}


Wireframes
{{ ![Wireframe](<excalidraw wireframe DRF.png>) }}


Colour Scheme

{{ /* CSS HEX */
--umber: #756658ff;
--seal-brown: #602C10ff;
--raw-umber: #9A6034ff;
--raisin-black: #1B171Eff;
--dutch-white: #F7E9C8ff; }}

Fonts

{{ [font: josefin sans](../../../Downloads/Josefin_Sans/JosefinSans-VariableFont_wght.ttf) }}


Submission Documentation


Deployed Project: https://crimson-pond-5974.fly.dev/

How To Run
In insomnia, access the above url. because its a secure site you will need to sign in with a username, password and email. you will be given an auth code that allows you access to the rest of the site. (you can save the authcode in your environment and use _.token to put it in all the different pages ;) In the GET requests you won't need to put any JSON in the request, but in the POST requests you do. The Projects post will look like this:
{
	"title": "str",
	"synopsis": "str",
	"goal": 150,
	"image": "url",
	"is_open": bool,
	"date_created": "2020-03-20T14:28:23.382748Z",
	"owner": 1
}  
for the pledges post you will need JSON that looks like this:
{
  "id": 1,
  "amount": 10,
  "comment": "Great project!",
  "anonymous": false,
  "project": 1,
  "supporter": 1
} 

Updated Database Schema
![Schema For Database](<crowdfunding/crowdfunding/images/schema for database.png>) 
I didn't much update the schema, because the basic relations haven't changed at all. 

Updated Wireframes
 ![Updated Wireframe](<crowdfunding/crowdfunding/images/Updated wireframe.excalidraw>) 
I now have a better idea of how the site will look with the react added.


How To Register a New User
In insomnia, in a POST user request, use this JSON:
{
	"username": "str",
	"password": "str",
	"email": "x@y.com"
}
Once you add a user you can sign in as that user, copy the auth token you are given and access all the pages by adding the auth token to the AUTH tab on each request. 

Screenshots

 A screenshot of Insomnia, demonstrating a successful GET method for any endpoint.
![Get Request](<crowdfunding/crowdfunding/images/Get request.png>)

 A screenshot of Insomnia, demonstrating a successful POST method for any endpoint.
![Post request](<crowdfunding/crowdfunding/images/Post request.png>)

 A screenshot of Insomnia, demonstrating a token being returned.

![Auth Token Request](<crowdfunding/crowdfunding/images/auth token request.png>)