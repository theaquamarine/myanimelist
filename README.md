myanimelist
===========

MyAnimeList plugin for FlexGet

This plugin is the fruit of rewriting fuzzylighs outdated plugin on
https://bitbucket.org/fuzzylights/plugins-for-flexget/wiki/Home

Mostly new code this will search for the text in the anime title instead of
parsing the link with regex

Syntax
======
The current version only allows to specify the username
``` YAML
myanimelist:
    username: username
```
Usage Example
============
``` YAML
preset:
  global:
    import_series:
    	from:
      		myanimelist:
      			username: edhaker13

tasks:
  test:
    mock:
      - {title: 'Entry title', url: 'http://some.location.com/'}
    accept_all: yes
```
Future Features
==============
If I have time I will try to code more functionality
And use a proper API like http://mal-api.com

Options to be enabled in the near future
- Choose which section to pull (by watching status)

`list: watching|completed|planned|on-hold|dropped`
- Select sorting method

`sort: by name|by score|`