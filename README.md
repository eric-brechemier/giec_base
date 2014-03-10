#GIEC Relational Database Model

##Installation
To run the model, you should prealably install latest ruby 2.\* and rubygems
(RVM is recommanded for this task).

```sh
rvm get stable
rvm use ruby --install --default
```

Hence, install dependencies with bundler :

```sh
gem install bundler
bundle install
```

This will install datamapper and its mysql adapter.

##Importing the database
From there, I will assume that you have with you the csv feed of the database (to put under feed/). Adapt the file config/database.example.yml with your db information and rename it to config/database.yml.

Then run the following command an wait (it usually takes 5-6 min).
```sh
./import
```

##Database Model
The datamapper model can be found under model/model.rb. You can use it to run complex queries on the database.

##Dependencies

	Ruby 2.0
	Rubygems
	bundler
	datamapper
	datamapper mysql adapter
