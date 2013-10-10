---
layout: post
title:  "Must. Type. Faster."
date:   2013-06-25 20:48:11
excerpt: "Speeding up the data-entry process. Some free JS plugins I made."
categories: blog
---

I've been working on an application recently which allows Solicitors and Legal Costs Draftsmen to quickly record time and budget forecast data. The application is very data-heavy, with multiple large forms throughout.

Obviously, with this model, anything that can speed up the data-entry process is a godsend. The user base is largely averse to using the mouse when entering data, tabbing through the fields as quickly as possible until they get to the end of the form, and then moving onto the next one.

One thing that was hindering this process was the standard date and time input fields available in HTML5. The data being entered is often copied from reports, or hand-written shorthand, and as such, does not always match the default format of the date/time fields, requiring the user to slow down, convert the date/time mentally and then enter. This may only take a couple of seconds per field, but when entering thousands of values a day, those seconds quickly add up.

Thus, the idea for [ DateMe](http://github.com/molovo/dateme) and [ TimeMe](http://github.com/molovo/timeme) was born. The idea being that a user can quickly stab out the data in whatever format it is presented to them, and it is then converted to a consistent value for storage in the database.

I couldn't find anything reliable (and lightweight enough) to do this for me, so I quickly coded up a couple of scripts, and after some user testing, it went down so well that I thought I'd release them for the public. Hopefully you find them useful.

#### Links
[ DateMe](http://github.com/molovo/dateme)  
[ TimeMe](http://github.com/molovo/timeme)