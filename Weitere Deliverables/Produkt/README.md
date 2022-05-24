# SwissDRG PSE-Projekt FS2022 🚁
Compare and review the differences in two chop catalogs.

Chopdiff is a web-based application to visualise and review the differences between two chop code catalogs of two years.
It allows the user to upload catalogs and transitions and calculates the differences and furthermore visualises the differences from one year to the following. 

## Versions

- Ruby: 3.0.2
- Postgres: => 12

---

## Setup

Installing rails and all other Gems:

```
bundle install
```
Installing react and other js libraries

```
yarn install
```
Creating the database

First, create a database user ("role") in Postgresql:

```sh
sudo su postgres
psql
```
Then in psql:
```postgresql
CREATE ROLE chopdiff PASSWORD 'chopdiff'  CREATEDB  LOGIN;`
```

Then, edit your `.env` file so it contains username and password of the user you just created. You can find a `.env.example` file in the repo which templates the used ENV variables.

`.env`:
```sh
# add local postgres user creds here 
LOCAL_DB_USER=yourUsernameHere
LOCAL_DB_PW=yourPasswordHere
```

Now, you can create the database:

```
rails db:create
```

You should now be ready to run the application locally.

---

## Running the application


```
./bin/dev
```

If you're using `rbenv`, don't forget to `rbenv rehash` to make sure installed gems are found by ruby. 

---

## Testing

### Backend

Running all Backend-Tests with 
```
rspec
```
or run a specific test 
```
rspec spec\path\to\test.rb
``` 
and add `--format documentation` if more output info is desired.
```
rspec spec --format documentation
```


To properly run the Tests psql will need admin rights to your test-database, these rights can be given with
```
alter user chopdiff with superuser
```
in the psql interface of the chopdiff_test database (access it with `psql chopdiff_test`).

Another useful command to load the test database with the fixtures data if some of the tests fail, because the database is empty is
```
RAILS_ENV=test FIXTURES_PATH="spec/fixtures" rails db:fixtures:load
```

To run the feature tests headless chrome is needed, or you change the specified browser in line 12 in `spec\rails_helper.rb`.

---
### Frontend
Frontend testing is done via the Jest framework.
```
yarn test
```
to run all frontend test suites and 
```
yarn test nameoftestfile
```
to test one specific test.
## Deploying

Describe deploying here