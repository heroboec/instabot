# Instabot
![Instabot is better than other open-source bots!](https://github.com/instagrambot/instabot/blob/master/docs/img/tag%20instabot.png "Instabot is better than other open-source bots!")
Cool Instagram scripts for promotion and API wrapper. Written in Python.
___
[![Telegram Chat](https://img.shields.io/badge/chat%20on-Telegram-blue.svg)](https://t.me/joinchat/AAAAAEHxHAtKhKo4X4r7xg)
[![Build Status](https://travis-ci.org/instagrambot/instabot.svg?branch=master)](https://travis-ci.org/instagrambot/instabot)

As you may know, Instagram closed its API in summer 2016. This Python module can do the same things without any effort.

README.md in [Russian](https://github.com/damirqa/instabot/blob/master/docs/ru/Readme_rus.md)

## What is it?

Instabot is a module for the Python language, which not only implements the wrapper over the Instagram API, but also various useful functions, such as "subscribe to the list of people", "like photos by hashtags", "unsubscribe from non-followers" and so on. Instabot is smart enough: [read](https://github.com/instagrambot/instabot/blob/master/docs/en/Filtration.md), for example, how it filters people on which it is going to subscribe.

## Ask a Question

* For error messages, use this [page](https://github.com/instagrambot/instabot/issues)
* If you have questions or would like to share your experience using Instabot, please write to our [Telegram](https://t.me/instabotproject)

## Installation

You can read the instructions for installing Instabot, following the link below
* Installing on [Windows](https://github.com/instagrambot/instabot/blob/master/docs/en/Installation_on_Windows.md)
* Installing on [Unix](https://github.com/instagrambot/instabot/blob/master/docs/en/Installation_on_Unix.md)

## How to use

Read the instructions for use [here](https://github.com/instagrambot/instabot/blob/master/docs/en/How_to_use.md)

## Update

Since the Instabot project is young and actively developing, updates will come out quite often. So if you stumble upon an error, do not rush to bang: try to update Instabot - maybe this error has already been corrected.

``` python
pip install -U instabot
```

## Developers

Developers better read the [documentation](https://github.com/instagrambot/instabot/blob/master/docs/en/For_developers.md)

## Highly recommended
*Make sure* you check out the example scripts [here](https://github.com/ohld/instabot/tree/master/examples). Chances are, your desired functions are *already there and ready to use*. Examples include *unfollowing non-followers*, *following competitor's followings and followers*, *liking posts of a specific hashtag*, and *more*...

If you have any ideas, please report them in the [Issues section](https://github.com/ohld/instabot/issues) or in our [Telegram chat](https://t.me/joinchat/AAAAAEHxHAtKhKo4X4r7xg).
**Your __contribution__ and support through __stars and reporting issues__ will be highly appreciated. After all, this project is dependent on your testing and support. :)**

## Docker
As long as docker is running on your machine you can build an instabot docker image like this
```
docker build -t instabot .
```

Then run your image with an example or your custom script:
```
docker run --name instabot -p 80:80 -i -t instabot python examples/like_example.py
```
