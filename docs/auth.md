---
id: auth
title: Authentication
sidebar_label: Authentication
---

Authentication is the process of recognizing a user’s identity. It is the mechanism of associating an incoming request with a set of identifying credentials. The credentials provided are compared to those on a file in a database of the authorized user’s information on a local operating system or within an authentication server.

CHI application handles authentication through passport.js.

### What is Passport.js?

Passport is authentication middleware for Node.js. As it’s extremely flexible and modular, Passport can be unobtrusively dropped into any Express-based web application. A comprehensive set of strategies supports authentication using a username and password, Facebook, Google, and more.

### Using passport to authenticate user by username and password

Once user submit the login form with its username and password. Those credentials is passed to passport for authentication using username and passport (refer the sample code below).

```
passport.use(new LocalStrategy({
  usernameField: 'email',
  passwordField: 'password',
}, function(email, password, done) {
  Users.findOne({$or: [{ email: email }, { username: email }]}, function(err, user){
		if (err) return done(err);
    if(!user) {
			return done(null, false, req.flash('errorMessage', 'No such user exists.'));
		} else if(!user.validPassword(password)) {
      user.incLoginAttempts(function(err){
        if(err) return done(err);
        return done(null, false, req.flash('errorMessage', 'Invalid email or password.'));
      });
    }
		return done(null, user);
	})
}));
```

In this file, we use the method validatePassword that we defined in the User model. Based on the result,we return the output from Passport’s LocalStrategy

### Using passport to authenticate user by Facebook

The Facebook strategy allows users to log in to a web application using their Facebook account. Internally, Facebook authentication works using OAuth 2.0.

In order to use Facebook authentication, you must first create an app at [Facebook Developers](https://developers.facebook.com/). After creating developer account, add FACEBOOK_CLIENT_ID and FACEBOOK_CLIENT_SECRET in .env to the client and secret received from Facebook developer account.

After clicking on **Login with Facebook** button, CHI application will redirect user to Facebook for authentication, to which Facebook will redirect users after they have approved access for your application. (refer sample code below)

```
passport.use(new FacebookStrategy({
    clientID: FACEBOOK_CLIENT_ID,
    clientSecret: FACEBOOK_APP_SECRET,
    callbackURL: "http://www.example.com/auth/facebook/callback"
  },
  function(accessToken, refreshToken, profile, done) {
    User.findOrCreate(..., function(err, user) {
      if (err) { return done(err); }
      done(null, user);
    });
  }
));
```

In this file, we return the output from Passport’s FacebookStrategy based on the result.

### Using passport to authenticate user by Google

The Googlr strategy allows users to log in to a web application using their Google account. Internally, Google authentication works using OAuth 1.0 OAuth 2.0.

In order to use Google authentication, you must first create an app at [Google Developers console](https://console.developers.google.com). After creating app, add GOOGLE_CLIENT_ID and GOOGLE_CLIENT_SECRET in .env to the client and secret received from Google developer console.

After clicking on **Login with Google** button, CHI application will redirect user to Google for authentication, to which Google will redirect users after they have approved access for your application. (refer sample code below)

```
passport.use(new GoogleStrategy({
    consumerKey: GOOGLE_CONSUMER_KEY,
    consumerSecret: GOOGLE_CONSUMER_SECRET,
    callbackURL: "http://www.example.com/auth/google/callback"
  },
  function(token, tokenSecret, profile, done) {
      User.findOrCreate({ googleId: profile.id }, function (err, user) {
        return done(err, user);
      });
  }
));
```

In this file, we return the output from Passport’s GoogleStrategy based on the result.
