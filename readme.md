# Heroku Buildpack: Ø

This buildpack does nothing. Use Ø if you need heroku to execute a binary.

## Usage

```bash
$ mkdir -p proj/bin

# make a run file that looks like this:
$ cat proj/bin/run
#!/usr/bin/env bash
echo hi from proj

# make a procfile that looks like this:
$ cat proj/Procfile
proj: bin/run

$ cd proj

$ heroku create -s cedar --buildpack http://github.com/ryandotsmith/null-buildpack

...

$ git push heroku master

...

$ heroku run proj
hi from proj
```