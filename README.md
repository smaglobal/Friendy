!<img width="500" alt="Screenshot 2022-12-16 at 01 20 42" src="https://user-images.githubusercontent.com/35616113/208000453-64bd0719-8364-4675-baf2-1fd0673485f4.png">
# Friendy

A Mobile Web App implemented in Ruby on Rails as a project during Le Wagon.

## Description

A simple donation application that lets user donate to donees using QR Code. A user can also add new donees to their dashboard where they can not only track their donations but can also report any emergencies or non-emergencies using live search feature. 

## Getting Started

## Install

### Clone the repository

```shell
git clone git@github.com:smaglobal/Friendy.git
cd project
```

### Check your Ruby version

```shell
ruby -v
```

The ouput should start with something like `ruby 3.0.3`

If not, install the right ruby version using [rbenv](https://github.com/rbenv/rbenv) (it could take a while):

```shell
rbenv install 3.0.3
```

### Install dependencies

Using [Bundler](https://github.com/bundler/bundler) and [Yarn](https://github.com/yarnpkg/yarn):

```shell
bundle && yarn
```

### Set environment variables

* Any sensitive data such as API keys can be set up in .env file e.g. (**process.env.STRIPE_SECRET_KEY)
* Require Stripe, Mapbox and Cloudinary APIs keys

### Initialize the database

```shell
rails db:create db:migrate db:seed
```

### Add heroku remotes (Optional)

Using [Heroku CLI](https://devcenter.heroku.com/articles/heroku-cli):

```shell
heroku git:remote -a project
heroku git:remote --remote heroku-staging -a project-staging
```

## Serve

```shell
rails s
```

## Deploy 

### With Heroku pipeline (recommended)

Push to Heroku staging remote:

```shell
git push heroku-staging
```

Go to the Heroku Dashboard and [promote the app to production](https://devcenter.heroku.com/articles/pipelines) or use Heroku CLI:

```shell
heroku pipelines:promote -a project-staging
```

### Directly to production (not recommended)

Push to Heroku production remote:

```shell
git push heroku
```
