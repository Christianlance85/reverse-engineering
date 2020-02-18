# reverse-engineering

--User Story--
As a learning developer
I want to walkthrough the source code
So that I am able to apply the learned tools to my own project.




--FILES EXPLAINED--

CONFIG
This directory holds the middleware, config, and the passport.

MIDDLEWARE

isAuthenticated.js { This restricts routes that the user is not allowed to visit if not logged in. if user is logged in, it continues with request };
config.json { This file contains the connection configuration to connect to server };

passport.js { This file holds javascript logic that tells passport we want to log in with an email address and password, as well as error bouncebacks if the login credentials don't match the database. };

MODELS

index.js { This file connects to our database and imports the users log in data };

user.js { requires "bcrypt" for password hashing. this makes our database secure even if compromised. Here we have Javascript that defines what is stored on our database including email and password.};

PUBLIC
JS:
login.js{This fiel provides the javascript login needed on the client-side to be able to log in as well as the api call to post.};
members.js{This file simply uses the api created to get the user data};
signup.js{This file containts the client-side javascript that allows users to signup.};

STYLESHEETS
login.html{ This provides the layout for the login page of our application.};
members.html{ This provides the layout for the members page of our application.};
signup.html{ This provides the layout for the signup page of our application.};

ROUTES

api-routes.js { This file contains routes for signing in, logging out and getting users specific data to be displayed client-side.};
html-routes.js { This file contains the routes that check whether user is signed in, whether user already has account etc, and sends them tio the correct html page};

package.json { contains all package info, node modules used, version info, as well as the dependencies needed before running the application};

server.js { This file requires packages, sets up PORT, uses sessions to keep track of the user's log in status, creates express and middleware, creates routes and syncs database / logs message in terminal on successful connection to server};

.gitignore{This file is simply ignoring the node modules used so when it is pushed to github, it doesn't push those files as well.};