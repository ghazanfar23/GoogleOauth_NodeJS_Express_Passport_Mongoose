Google Oauth using passport strategy

1)Please install all packages availabale in package.json file.
 "dependencies": {
    "cookie-session": "^2.0.0-beta.3",
    "express": "^4.16.3",
    "mongoose": "^5.3.1",
    "nodemon": "^1.18.4",
    "passport": "^0.4.0",
    "passport-google-oauth20": "^1.0.0"
  }

2) Create accounts for googleAPI's, mLab and Heroku(if you want to host remotely).
3) Note: if you wanna host on heroku then do not install packages. Heroku will read pakage and install them on server.

4) create config folder in root directory and make a file called keys.js and use your own keys inside quotes.
module.exports = {
  googleClientID:
    "",
  googleClientSecret: "",
  mongoURI:
    "",
  cookieKey: ""
};

Endpoints:
Callback: localhost:5000/auth/google/calback
login/Authentication: localhost/5000/auth/google
get google id of logged in user: localhost/5000/api/current_user
logout: localhost/5000/auth/logout
