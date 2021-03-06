Sinatra::WebInspector
=====================

The WebInspector allows you to inspect a running [Sinatra](http://sinatrarb.com) app.
Just browse http://localhost:4567/\_\_inspect\_\_

When used with BigBand, it will – per default – only be activated in development mode.

BigBand
-------

Sinatra::WebInspector is part of the [BigBand](http://github.com/rkh/big_band) stack.
Check it out if you are looking for other fancy Sinatra extensions.


Installation
------------

_Note:_ CSS has not yet been imported from BigBand, so you won't really enjoy this.

    gem install sinatra-web-inspector --prerelease

Usage
-----

Classic style:

    require "sinatra"
    configure(:development) { require "sinatra/webinspector" }

Modular style:

    require "sinatra/base"
    require "sinatra/webinspector"
    class Foo < Sintra::Base
      configure(:development) { register Sintra::WebInspector }
    end
