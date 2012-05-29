Fone-U for the Asterisk PBX
===========================

Using Fone-U APIs from the Asterisk PBX.

See http://fone-u.com

Dialplan integration
--------------------

The initial integration script for Asterisk and FreePBX is available; this makes it
simple to use Fone-U as an optional trunk when dialing out. Requires `curl` but 
it will likely be altready compiled within your Asterisk server.

You can find this within the directory `dialplan` of this project. 

This approach is very simplicistic and just tries one route if present. Will likely
work in the majority of real-life cases.

AGI integration
---------------

We also plan to release:

- An AGI script with flexible routing and retrying



Useful links
------------

 - The Fone-U API @ http://fone-u.com/api.jsp
 - The Asterisk AGI interface @ http://www.voip-info.org/wiki/view/Asterisk+AGI

Seems like the API servers at Fone-U are having some issues. It's a pity 
because this could be very interesting (like ENUM but way easier to use).
