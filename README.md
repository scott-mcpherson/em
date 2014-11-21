To see the most current and original repo, please visit https://github.com/EventedMind/em 

# em

A command line scaffolding tool for Meteor applications. It automatically
creates project structure, files and boilerplate code. The project structure
mimics that of the EventedMind publishing platform.

## Installation

Install the em command line tool globally so you can use it from any project
directory.

```sh
$ npm install -g meteor-em
```

## Pre-Reqs

You'll want to have [Iron Router](https://github.com/eventedmind/iron-router)
installed. Also, this command line tool just handles scaffolding for now. `mrt`
and `meteor` are different command line tools. Hopefully, sometime in the near
future we can enhance the `meteor` command line tool to be pluggable!

## Usage

Just type ```em``` from the command line and you'll see the various top level
commands. Then type ```em generate``` or ```em g``` to see a list of generators.

You can initialize your project structure like this:

```sh
$ em init
```
A config file will be generated in your project — `.em/config.json`, and you will
be able to specify what types of files will be created for you when you generate
a view resource. You can also specify alternative file extensions, e.g. .jade, .sass, and .coffee:
```json
{
  "view": {
    "html": {
      "create": true,
      "extension": ".html"
    },
    "css": {
      "create": true,
      "extension": ".css"
    },
    "js": {
      "create": true,
      "extension": ".js"
    }
  }
}

```

Then you can generate various resources. Here are a few examples:

```sh
$ em g:scaffold todos
$ em g:view todos/todo_item
$ em g:controller webhooks/stripe --where "server"
$ em g:route todos/todo_show
```

## Contributing

This is an early alpha project and any thoughts and contributions are welcome.

## License
MIT
