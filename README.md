# makerMessage
Send a message to IFTTT's [Maker 
Channel](http://blog.ifttt.com/post/121786069098/introducing-the-maker-channel)

# Installation

1. Install [Groovy](http://www.groovy-lang.org/download.html)
1. Clone this repository
1. Activate IFTTT's [Maker Channel](https://ifttt.com/maker)
1. Add your maker channel secret key to ~/.makerMessage

# ~/.makerMessage

This is the script's config file.  Right now, it only contains one value: your 
secret key for the Maker channel:

```
ifttt.secret = "<your secret key>"
```

Naturally, you should keep this file a secret.  Make it inaccessible to others.

# Running

```
makerMessage [--value1=<value1>] [--value2=<value2>] [--value3=<value3>] <event>
```

IFTTT's Maker Channel supports 3 parameters.  The first of which is an event 
name.  The event name is always required value1 through value3 are optional and 
can be used within your IFTTT recipes to send data to other channels.

# Exit status
makerMessage returns '1' if it can't make a request.  If the request is 
successful, it returns '0'.  If the request itself fails, the HTTP status code 
of the request is returned.
