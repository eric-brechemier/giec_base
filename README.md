#GIEC Relational Database Model

##Installation
To run the model, you should prealably install latest ruby 2.\* and rubygems
(RVM is recommanded for this task).

```sh
rvm get stable
rvm use ruby --install --default
```

Note: to allow compiling of the native extension for do_mysql gem,
[you need to install the development package for MySQL]
(http://stackoverflow.com/questions/1857059/cant-install-do-mysql-gem).

This installation step depends on your system:

```sh
# using apt-get (Ubuntu/Debian)
sudo apt-get install libmysqlclient-dev

# using RPM (Red Hat)
sudo yum install mysql-devel

# using brew (Mac OS X)
brew install mysql
```

Hence, install dependencies with bundler :

```sh
gem install bundler
bundle install
```

This will install datamapper and its mysql adapter.

##Importing the database
From there, I will assume that you have with you the csv feed of the database
(to put under feed/). Adapt the file config/database.example.yml with your db
information and rename it to config/database.yml.

Then run the following command an wait (it usually takes 5-6 min).
```sh
./import
```

##Database Model
The datamapper model can be found under model/model.rb. You can use it to run
complex queries on the database.

##Dependencies

	Ruby 2.0
	Rubygems
	bundler
	datamapper
	datamapper mysql adapter
