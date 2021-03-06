[![Build Status](https://travis-ci.com/DARK-art108/TellTodo.svg?branch=main)](https://travis-ci.com/DARK-art108/TellTodo)
![GitHub forks](https://img.shields.io/github/forks/DARK-art108/TellTodo?style=social)
[![forthebadge made-with-python](http://ForTheBadge.com/images/badges/made-with-python.svg)](https://www.python.org/)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)
[![Open Source Love svg1](https://badges.frapsoft.com/os/v1/open-source.svg?v=103)](https://github.com/ellerbrock/open-source-badges/)
[![ForTheBadge built-with-love](http://ForTheBadge.com/images/badges/built-with-love.svg)](https://GitHub.com/Naereen/)

# TellTodo🤖 🦜

<p align="center">
  <img width="800" height="500" src="utils/bo.gif">
</p>


## Meet TellTodo👋

TellTodo is a Python and a FaunaDB powered telegram bot which helps you to manage your daily task with the help of Todo-List, you can ask TellTodo to perform the following operations:

- [x] Add/Create your daily task in the todo list
- [x] Check your status of the task weither it is completed or not
- [x] Update your todo list task status to completed.
- [x] List your Todo List
- [x] Delete your Todo list/Task


## How TellTodo is Built?

TellTodo uses Python 3.8 Programing Language and one of the Latest and a Serverless Database which is FaunaDB.

### FaunaDB

<p align="center">
  <img width="1000" height="500" src="utils/f.png">
</p>


Fauna is a ***Serverless Database***, a serverless database is one where all maintenance and operational responsibility is outside of a developer or application’s concern, and all traffic/CRUD is accommodated with on-demand scaling. This reduces the load and effort put into managing the database resources, especially when the application begins to scale to support a large number of users.

There are a lot of advantages of picking a serverless database for your application aside from reducing work in managing database resources. They include:

* Database operational cost reduction
* Real-time database access
* Increase in productivity (since the burden of database management is removed)
* Infinite scalability
* Improved database security

we now know Fauna is a serverless database, but **how does it store and handle data?** At its core, Fauna is a **document database** that offers two interfaces, ***GraphQL*** and the ***Fauna Query Language (FQL)***. Databases can store collections, indexes, and even other databases (yay multi-tenancy!). Within collections are documents, which by default, don’t have strict schema requirements. Fauna is capable of handling a variety of data types (e.g. temporal) but is particularly impressive for having first-class support for relational data. We’ll be exploring most of this together momentarily, but if you’re eager to learn even more, check out the [Fauna documentation](https://docs.fauna.com/fauna/current/index.html)!

### Getting Started with TellTodo Local Setup

**Setup FaunaDB:**

1. Create the account on [FaunaDB](https://dashboard.fauna.com/accounts/register)

2. Click on `New Database`

<p align="center">
  <img width="700" height="400" src="utils/dbs.png">
</p>

3. After creating a Database, Click on `Collections` then `New Collection`

<p align="center">
  <img width="700" height="400" src="utils/col.png">
</p>

Give the name to the collection as `users` as users name is default with our bot.

4. Similarly, create another new collection named as `todo` as todo is default with our bot.

5. Now, move to `Index` and create a `New Index` and make sure that the ***Source Collection*** is `users` and ***Terms*** is `data.id` with a ***Name*** `users`.

6. Similarly create `New Index` ***Source Collection*** is `todo` and ***Terms*** is `data.user_id` with a ***Name*** `todo`

After a sucessfull setup your Index and collection will look like:

<p align="center">
  <img width="700" height="400" src="utils/index1.PNG">
</p>

<p align="center">
  <img width="700" height="400" src="utils/index2.PNG">
</p>

<p align="center">
  <img width="700" height="400" src="utils/fauna1.PNG">
</p>

After setting up the whole database, now you need to get the `Security Key` so go to the `Security` section and get your `Security Key`.

Now, your FaunaDB is setup and ready to use!!

### Create your Telegram Bot

* Ping @BotFather on Telegram.
* Send the message /start
* Read the instructions and make a new bot for your personal testing by /newbot command.
* Give a suitable name and username to the bot.
* You’ll get your bot API token as 89xxxxxxx:xxxxxxxxxxxxAAHmf32ZghS-cqxBLfnkUx9VwoXeOIRlnUQ.
* Replace and add your telegram_token_key = "YOUR_TELEGRAM_KEY" in `config.py` file.
* Replace and add your fauna_secret = "your_fauna_secert" in `config.py` file.

### Build and Execute Bot

* Install all dependencies using `pip install -r requirements.txt`
* Run your bot using `python3 bot.py or python bot.py`
* Ping your bot at @<username_set>. You’ll find the bot up and running.

### Guide to Run TellTodo Bot

The bot accepts the following commands:

* `/start`: To start the bot
* `/add_todo`: To add todo or task
* `/list_todo`: To list the todo or task with status

You can add as many task or todo you want!!

For executing the bot first time you need to drop a `/start` cmd so that your entry will be done in the faunadb,after that you can proceed other cmd's of adding , deleting,updating and listing todo's.

You can see your queries and lastcmd's in faunadb dashboard in JSON formats, you can even query the database using String,Number or FQL.

***Ping our existing 24 * 7 Active bot using @faunadbtest in telegram (for testing purpose only)!!***













