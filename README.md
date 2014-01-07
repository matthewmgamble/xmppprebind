XMPP Prebind for Java
====================

This class is for [prebinding](http://metajack.im/2009/12/14/fastest-xmpp-sessions-with-http-prebinding/) a XMPP Session with Java.

The code is based on the Candy Chat XMPP Prebind code for PHP (https://github.com/candy-chat/xmpp-prebind-php)
Usage
=====
* Clone the repo

Example usage:
```java
/*
 * Create a new XMPP Object with the required params
 *
 * @param String boshHost Jabber Server Host
 * @param String xmppDomain XMPP Domain
 * @param String boshUri    Full URI to the http-bind
 * @param String resource   Resource identifier (example "Work")
 * @param String boshPort	Bosh Port Number (usually 7070)
 * @param boolean   useSsl     Use SSL 
 * @param boolean   debug      Enable debug
*/      
	XMPPPrebind xmppPrebind = new XMPPPrebind(boshHost, xmppDomain, boshUri, resource, boshPort, useSsl, debug);
        xmppPrebind.connect(username, password);
        xmppPrebind.auth();
        SessionInfo sessionInfo = xmppPrebind.getSessionInfo();
        System.out.println("jid:" + sessionInfo.getJid());
        System.out.println("sid:" + sessionInfo.getSid());
        System.out.println("rid:" + sessionInfo.getRid());
```
* You should now have a working prebinding with Java!

Debugging
=========
If something doesn't work, you can enable Debug.

Here be dragons
========
This class is in no way feature complete. There may also be bugs.  

Thanks!
