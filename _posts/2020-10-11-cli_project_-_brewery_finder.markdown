---
layout: post
title:      "CLI Project - Brewery Finder"
date:       2020-10-11 21:09:34 +0000
permalink:  cli_project_-_brewery_finder
---


Hi everyone! 

Today I want to share some of the things I learned across this project and also 
some of the challenges I faced during the process of creating my first CLI application
that stnds for Command-Line Interface, so we are going to interact through the command prompt.

## Git and GitHub

First you need to have a clear concept of how to use git, because it is going to be 
our foundations to make meaningful commits. The rule of thumb is making commits every 
15 lines of continuing code, and there is no minimum, even 1 or 2 lines can be enough!


These are the commands to push a new commit to our repository:
```
git add .

git commit -m "your message"

git push origin main
```

I had some issues with this command because most of the information about making commits, normally call
the "master" branch and for a better inclusive language GitHub change this command for "main" and I was just so cunfused when I was trying to make my commits. The update of "main" became effective one week before I start my project and that's why it was difficult to realize.

## Enviroment File

When I start using a specific file to contain all the gems and require links everything became so much easier to read,
and identify. I look at it like the index page of a book because you just need to look at one file  that makes it easier to place, identify and having a cleaner code. 

```
require 'pry'
require 'net/http'
require 'json'
require 'colorize'

require_relative './lib/api'
require_relative './lib/cli'
require_relative './lib/breweries'
```


## Classes

Classes are one of my favorites and more important methods because once you start working with Objects instead 
of just filling a hash or array with information you get a precise way to track objects because they became uniq in our program.

One common issue is when we have two different variables who share the same information, lets suppose we have 2 different persons who have the same name and birth date and those 2 'key' values are the same ones we are using to identify the users. We are facing a potential issue when we want to compare those variables because they can be interpretated as the 'same' even when they are refering to different persons.

Thats when we instantiate an object, even if they share the very same information, each one points to their own object id that we can recall with #object_id. and we can test that there are not 2 objects with the same id in the next statement:

```
Object.new.object_id  == Object.new.object_id  # => false
```



## Conclusion and Experience

Creating your first CLI program from scratch can be overwhelming, but as long as you have a structured way to test all your code before moving on with more blocks and undestand the basics of how and where you organize your files nothing is impossible.


Link to quick guide to make your CLI from scratch:
```
https://levelup.gitconnected.com/building-a-ruby-cli-gem-from-scratch-fca59acda169
```

Link for debugging with PRY instructions:
```
https://learn.co/tracks/online-software-engineering-structured/procedural-ruby/variables-and-methods/debugging-with-pry
```


