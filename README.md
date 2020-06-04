## Authoring Environment Setup

When setting up your machine for the first time, run:

```bash
#install Ruby Version Manager (rvm.io/rvm/install)
\curl -sSL https://get.rvm.io | bash -s stable
# restart terminal or run the following source command:
source ~/.rvm/scripts/rvm
# install Ruby 2.7 and the needed dependencies
rvm install 2.7
rvm use 2.1 --default
gem install bundler
# make sure you're in the root of your clone of this repo and run
bundle install
```

Then when authoring, run:

```bash
bundle exec jekyll serve
```

You can preview your changes by visiting `http://localhost:4000`

## Docker Instructions for Authoring

Don't want to install a bunch of stuff and don't mind the overhead of using Docker? Do this instead:

```bash
docker build -t blockdocs .
docker run -p 4000:4000 -ti -v "$(pwd)":/usr/src/app blockdocs
```
