# Rails for CI Docker Image
build from [official image](https://github.com/docker-library/ruby)

## Features
A few packages are installed:

- mysql-client
- postgresql-client
- sqlite3
- nodejs
- yarn (via npm)
- phantomjs (via npm)
- imagemagick
- mecab
- libmecab-dev
- mecab-ipadic-utf8
- unzip

and npm packages are installed:

## Usage
```
docker run -d heathrow/rails-ci:latest
```

[https://github.com/docker-library/ruby](https://github.com/docker-library/ruby)
