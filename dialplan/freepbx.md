Using Fone-U from FreePBX
-------------------------

* Create a Fone-U account on http://fone-u.com
* A account can list multiple numbers and each has its own APi key. Get the API key for the 
  PSTN number that is used for your PBX.
* Edit `/etc/asterisk/extensions_custom.conf` and add the contents of the file  `freepbx_addon.conf` 
* Change the variable `FU_APIKEY` to your API key
* Now go to the FreePBX admin page; create a new trunk called "Fone-U"
  * Type: Custom Trunk
  * Dial rules: "." (just put a dot in there)
  * Custom Dial String: `Local/$OUTNUM$@foneu-simple`
  * Save your new Trunk
* Now go to the FreePBX admin page; select your outbound route (or add a new outbound route)
  * Put the new trunk "Fone-U" as the first trunk it is used when dialing out
* Apply changes to Asterisk

Now, when you dial out, your PBX will try dialing through Fone-U first; if it does not find a valid
route, it dials though other trunks.

It was easy, wasn't it?

