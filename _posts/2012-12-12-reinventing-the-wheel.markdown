---
layout: post
title:  "Reinventing the wheel"
date:   2012-12-12 13:35:30
excerpt: "Simplifying the signup process"
categories: blog
---

### Simplifying the signup process

I've been working on an app recently that has a simple aim, speed and simplicity. Without revealing to much information, the app allows the user to send emails from the account with which they sign up. As such, email verification in a secure way was an imperative requirement, and I wanted to see if there was any way in which I could reduce the signup procedure to as few clicks as possible, and still maintain a good level of security.

As the best way for the user to see a sample of the emails that could be sent with the application was to send a sample, and explain the features within that, I also integrated this into the signup procedure. As a result, the single call to action on the page is a single button, with the text "See a sample/Sign up". On mouseover this expands to the width of the container, the text fades out, and is replaced by a single email input box. The text below also fades in, and explains how it works to the user:

> Just enter your email here, and we'll send you an example of what you can create with - name removed -. If you want to sign up, just click the link in the email and your account will be created automatically.

> Since - name removed - will send emails from the address you provide above, we are doing it this way so we can be sure it's your email, cos we can't let you go around pretending to be the President now can we? We won't store any details until you click the link in the email, so if you're not interested, just ignore it and we'll forget you were ever here. *Who are you again?*

But how to make this work in practice, and still maintain security?

When I say above that the email is never stored, I meant it. When an email is entered, two things happen. Firstly a 64 character random string is created. This is then added as a new row in a single column table containing all the activation codes currently in use. This random string is also added to the URL for the signup link in the email, along with the email itself. The only time the email is EVER associated with the string is in that one URL.

Upon the user clicking the link, the app opens in the browser, and scans the activation code table for the string in the URL. If it is found it is immediately deleted, and a new account is created with the email that was in the URL. If the email is ignored, the code is deleted after 7 days, with the app still blissfully unaware of the email with which it is connected.

Stopping URL harvesting from being used to hit the app with repeated random strings in an attempt to break it is accomplished by allowing no more than 5 calls to that URL per IP address per day. It would take years to correctly match a random string with this limitation.

Account creation is done by creating a new session variable with the users email, and they are prompted with a password and confirmation box. The account is only then created when a valid password is entered on this screen, and a new, different session variable is created which allows the user to access to the application, as would happen during normal login.

So there you have it, feature demonstration, email verification and signup in just three clicks.

The app is still in development so I'd be interested in hearing your thoughts on possible security issues, and if there's anything I've missed. Feel free to ask any questions in the comments below.