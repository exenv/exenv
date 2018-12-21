# Groom your app’s Elixir environment with exenv. [![Build Status](https://travis-ci.org/exenv/exenv.svg?branch=master)](https://travis-ci.org/exenv/exenv)

Based totally on the GREAT [rbenv](https://github.com/rbenv/rbenv)

rbenv's documentation largely applies here as well


## Installation

### Basic GitHub Checkout

This will get you going with the latest version of exenv and make it
easy to fork and contribute any changes back upstream.

1. Check out exenv into `~/.exenv`.

    ~~~ sh
    $ git clone https://github.com/exenv/exenv.git ~/.exenv
    ~~~

    Optionally, try to compile dynamic bash extension to speed up exenv. Don't
    worry if it fails; exenv will still work normally:

    ~~~
    $ cd ~/.exenv && src/configure && make -C src
    ~~~

2. Add `~/.exenv/bin` to your `$PATH` for access to the `exenv`
   command-line utility.

    **For bash**

    ~~~ sh
    $ echo 'export PATH="$HOME/.exenv/bin:$PATH"' >> ~/.bash_profile
    ~~~

    **For zsh**

    ~~~ sh
    $ echo 'export PATH="$HOME/.exenv/bin:$PATH"' >> ~/.zshrc
    ~~~

    **For fish shell**

    ~~~ sh
    $ echo 'set PATH $HOME/.exenv/bin $PATH' >> ~/.config/fish/config.fish
    ~~~

3. Run `~/.exenv/bin/exenv init` for shell-specific instructions on how to
   initialize exenv to enable shims and autocompletion.

4. Restart your shell so that PATH changes take effect. (Opening a new
   terminal tab will usually do it.) Now check if exenv was set up:

    ~~~ sh
    $ type exenv
    #=> "exenv is a function"
    ~~~

5. _(Optional)_ Install [elixir-build](https://github.com/mururu/elixir-build), which provides the
   `exenv install` command that simplifies the process of installing new Elixir versions

#### Upgrading

If you've installed exenv manually using git, you can upgrade your
installation to the cutting-edge version at any time.

~~~ sh
$ cd ~/.exenv
$ git pull
~~~
