
# Budget Munchies
Welcome to the Budget Munchies home page!

# TABLE OF CONTENTS

* [Overview](#overview)
* [User Guide](#user-guide)
* [Current State of the Project](#current-state-of-the-project)
* [Project Pages](#project-pages)
* [Deployment](#deployment)
* [Developer Guide](#developer-guide)
* [Team](#team)


# Overview
This project offers a solution for college students on the hunt for recipes that are cheap, easy to make, and have limited ingredients. 
Users will be able to share recipes that have information such as cost per meal, appliances needed, dietary restrictions, time it takes to make, etc. 

Students will be able to search, browse, and post recipes to the site. The recipes should at least include full ingredients list, appliance used, a picture of the finished meal, and the directions itself. There will be a favorite recipes page and the landing page will have some of the weekly favorites from the users. 

# User Guide
## Landing (Signed Out)
Upon visiting the Budget Munchies site, you will arrive on the initial landing page, without user sign in.

<img src="/m2landing.png">
## Sign-in Page
This is the sign in page that you will see after clicking login. 
<img src="/m2signin.png">
## Landing (Signed In)
This is the landing page after user sign in. Sign in enables you to see additional pages and elements. 
<img src="/m2signedinlanding.png">
## Add recipe Page
This page shows the add recipes function. Recipes can be submitted to the website and much include specific details such as appliance, type of meal, dietary restrictions, etc. 
<img src="/m2add.png">
## List Recipes Page
This page will show a list of recipes. It currently shows a stock table database. 
<img src="/m2list.png">
## Browse Recipes dropdown Menu
Brose recipes is a dropdown menu that allows you to click on the specific type of meal you are searching for. 
<img src="/m2browse.png">
## Search
You will be able to search for specific recipes. This also shows our 'not found' page becuase search is currently not implemented. 
<img src="/m2search.png">

# Design Mockups
### Mockup landing page
This is the original team favorite design of our landing page. Our team all created test landing page mockups and we went with this one for the design and color scheme. 
<img src="/land.png">

### Alternative landing page
This is an alternative of the lading page. It looks similar to the original landing page with some tweaks. This was created after deciding the colors and design we wanted to follow.  
<img src="/signin-signup.PNG">

### Mockup user home page
This is the mockup design for the user home page. When the user signs in, or signs up, this is the page they will be directed to after. 
<img src="/user-home.PNG">

### Mockup add recipe page
This is a mockup of a page where users can add recipes. 
<img src="/add-recipe.PNG">

# Deployment 

[Budget Munchies deployed on Digital Ocean](https://budgetmunchies.xyz/#/)

## Testing and Continuous Integration
![ci-badge](https://github.com/budget-munchies/budget-munchies-project/workflows/ci-budget-munchies-project/badge.svg)

<a href="https://github.com/DevExpress/testcafe">
    <img alt="Tested with TestCafe" src="https://img.shields.io/badge/tested%20with-TestCafe-2fa4cf.svg">
</a>

# Current state of the project
  Please view the [User Guide](#user-guide) for the current state of the project. 
# Project Pages

### M1
[Milestone 1 Project Board](https://github.com/budget-munchies/budget-munchies-project/projects/1)

### M2
[Milestone 2 Project Board](https://github.com/budget-munchies/budget-munchies-project/projects/2)

### M3

[Milestone 3 Project Board](https://github.com/budget-munchies/budget-munchies-project/projects/3)

# Github Organization

[Budget Munchies](https://github.com/budget-munchies)

# Developer Guide
This guide is an explanation of how to download, install, and run the system via github, meteor, and terminal/command line.

## Installation

First, [install Meteor](https://www.meteor.com/install).

Second, download [Budget Munchies Repository](https://github.com/budget-munchies/budget-munchies-project) to your computer using the green code button. You can download it as a zip file, or you can click open with GitHub desktop. 

Third, cd into the app/ directory of your local copy of the repo, and install third party libraries with:

```
$ meteor npm install
```

## Running the system

Once the libraries are installed, you can run the application by invoking the "start" script in the [package.json file](https://github.com/ics-software-engineering/meteor-example-form-react/blob/master/app/package.json):


```
meteor npm run start

> meteor-example-form-react@ start /Users/philipjohnson/github/ics-software-engineering/meteor-example-form-react/app
> meteor --no-release-check --settings ../config/settings.development.json

[[[[[ ~/github/ics-software-engineering/meteor-example-form-react/app ]]]]]

=> Started proxy.
=> Started MongoDB.
W20190718-11:08:30.749(-10)? (STDERR) Note: you are using a pure-JavaScript implementation of bcrypt.
W20190718-11:08:30.770(-10)? (STDERR) While this implementation will work correctly, it is known to be
W20190718-11:08:30.771(-10)? (STDERR) approximately three times slower than the native implementation.
W20190718-11:08:30.771(-10)? (STDERR) In order to use the native implementation instead, run
W20190718-11:08:30.771(-10)? (STDERR)
W20190718-11:08:30.771(-10)? (STDERR)   meteor npm install --save bcrypt
W20190718-11:08:30.771(-10)? (STDERR)
W20190718-11:08:30.771(-10)? (STDERR) in the root directory of your application.
=> Started your app.

=> App running at: http://localhost:3000/
```


### Note regarding "bcrypt warning":

You will get the following message when you run this application:

```
Note: you are using a pure-JavaScript implementation of bcrypt.
While this implementation will work correctly, it is known to be
approximately three times slower than the native implementation.
In order to use the native implementation instead, run

  meteor npm install --save bcrypt

in the root directory of your application.
```

On some operating systems (particularly Windows), installing bcrypt is much more difficult than implied by the above message. Bcrypt is only used in Meteor for password checking, so the performance implications are negligible until your site has very high traffic. You can safely ignore this warning without any problems during initial stages of development.

### Viewing the running app

If all goes well, the application will appear at [http://localhost:3000](http://localhost:3000).

### ESLint

You can verify that the code obeys our coding standards by running ESLint over the code in the imports/ directory with:

```
meteor npm run lint
```

### Testing with TestCafe

This application has continuous integration and testing with TestCafe. Tests should run automatically, otherwise you need to Control C out of the terminal/command window, and invoke "meteor npm run testcafe" insdie the app directory. This will run the created tests. 

### Prerequisites

To best understand this application, it is useful to familiarize yourself with:

* [Meteor Application Template React](http://ics-software-engineering.github.io/meteor-application-template-react/). This sample application illustrates conventions for directory layout, naming conventions, routing, integration of Semantic UI, and coding standards. Meteor-example-form is based on this template, so we won't discuss any of these issues here.

* [Semantic UI React](https://react.semantic-ui.com/). We use Semantic UI for this template.

* [Uniforms](https://uniforms.tools/). Uniforms is a library for simplifying form management with React, and includes built-in integration with Semantic UI.


# Mockup ideas
* Landing page
* User home page
* Admin home page
* User profile page
* Add Recipe page
* Filter/browse recipes Page
* Vendor info page

# Possible Extras
* Maps for locating vendors
* Ratings and review system for recipes
* Ratings and review system for vendors
* Notification system for vendors when new items are posted in recipes so they can update their listing to indicate whether they stock it or not
* Notification system when price for a recipe drops substantially (i.e. a vendor puts an item on sale.)

# Team
[Sydney](https://sydney-c7.github.io), [Kieran](https://kieran-k.github.io), [Marissa](https://marissahalim.github.io), [Nanami](https://nakimoto.github.io)
