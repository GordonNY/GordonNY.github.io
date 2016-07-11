---
layout: post
title:  "CLI Data Gem"
date:   2016-07-11 14:48:52 -0400
---


This is my first assignment in Flatiron School. 

# About
The project will scrap data from Google, Yelp, and Zagat, and gather the data together, by analyzing the data, to give user the best restaurants for specific food like pad thai.

# Technologies

1. Github, working as a team
2. Google API
3. Object Oriented Ruby

# Details

**1. Github**

I have never used Github working with other people. In order to practice it in a team environment, I did the pair programming with Unmi, one of my classmates, which truely allowed me a better understanding of how to use Github in a team.

How to use Github in a team:
1). Unmi created a repo as the root repo and added me to the contributors. I have two choices, either Fork this the root repo or just pull the repo to my local. In order to have a deep understanding of how it works, I forked the root repo, and then clone the repo to my local.
2). After cloned the repo under my account, I started writing codes. 
3). I think it is better to create a branch for every big change using 'git checkout -b branch-name'. The reason is that, by adding changes to the branch, I am able to fix the code conflicts before create a pull request to the root repo. Before I merge the branch into my master branch, I can create a pull request to update my master branch from the root repo master in order to keep my master updated. Then I can merge the branch into my master branch, and fix the conflicts.
4). After finishing codeing, fixing code conflicts, and merging the branch into my master branch, I can create a pull request to the master branch of root repo.
5). Command:
  git clone ...
  git checkout -b branch-name
  git add .
  git commit -m "description"
  create pull request, base fork: my master, head fork: root master
  git pull origin master
  git push origin branch-name or git checkout master, git merge branch-name
  fix conflicts
  create pull request to send my code to root repo master

**2. Google API**
I used a Gem called google_places to send requests to Google, and Net::HTTP.get_response(URI.parse(request_uri)) to get restaurants' details.
Structure: 
class Google::URIHelper:
top10RestaurantInfoWith(location:, food:)
\_requestTop10RestaurantInfo
\_parseRestaurantInfo(restaurants)
\_generateRestaurantInfoHash(restaurant)
\_getRestaurantDetailWith(place_id)
class Google::Scraper:
self.scrapRestaurantInfoWith(location:, food:)

**3. Object Oriented Ruby**
We create a class Restaurant to hold the restaurant information, and used mass assignment way to initialize it.

Github:
https://github.com/GordonNY/findthebestfood



