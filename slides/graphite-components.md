## The Three Parts

`carbon` : a server listening for incoming stats on TCP port 2003 and responding to queries on TCP port 7002

`whisper` : a time series database management system

`graphite-web` : a [django](https://www.djangoproject.com/) web app that renders graphs using [cairo](http://cairographics.org/pycairo/)