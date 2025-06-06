---
title: 'Get started with PGP!'
summary: Get started with PGP
showToc: true
tocOpen: true
---
### What is "PGP"?
PGP stands for "[Pretty Good Privacy](https://en.wikipedia.org/wiki/Pretty_Good_Privacy)", and it is a program used to encrypt messages. It is free to use, and open-source (the code is public). It was written by Phil Zimmermann in the 1990s.
### What do you mean by "encrypted messaged"?
An encrypted message means the message isn't read as clear text. It's the difference between this:
```txt
This is a sample.

This is a sample text file.  I created it with an editor.  If it were
an actual message, it would contain some useful information.

This has been a sample.
```
and this:
```pgp
-----BEGIN PGP MESSAGE-----
Version: 2.6.2

hIwD1vwet/TdJfEBBACdcCPkNI3kRwYqtHUyfpvVAY5rt+Lb9P6EztNd4sYq9egV
CZjfqcCn36XZmYPbbO6nZbl992kPRFzTgCRszKNPtlk6Wa93AqXs3KCZp+4emXQh
7moE+XTf4QUGJZ2L3w/sSNs5WFkZRIbto0ivK1aRlX1XTqhPqo9HbgEfElBVUaYA
AACQEWaOS3/h6BVLHTfXaK20vmLcg9BUisB5RDvYGLZv9XFwHMMjctFJJQYnWIOp
+7LLkmNO5fE48rWh0EOAwjAeduGzJGQb4yiE7OlxoESmmTJQ+qO1K2nDz8Stk3a6
WvAQJrpEUY7Og8QGlQQRPKl2F++j6XbIhZ27OeYqJp+vgylUd874KDMCcTrzF3ph
/Qfi
=xTV9
-----END PGP MESSAGE-----
```
*Example provided by [Rutgers' University's Computer Science Department](https://people.cs.rutgers.edu/~watrous/pgp-eat.html).

It's much harder to make any sense out of the encrypted text, right? Well, that's the point!

### But GMail and WhatsApp tell me their website and my messages are encrypted!
Sure, the website is encrypted, and so are your message (to some extent). But the idea behind using PGP, or some equivalent, isn't to complicated matters by adding more layers of encryption; PGP is a great tool to mask your messages in the case of a leak. Websites are hacked into, and their data is dumped online, all the time. What good would a chatlog be if it was filled with encrypted text? Very little. If the messages were in plain text, then it would be worth a lot (at the cost of your privacy). Moreover, PGP offers a lot more than mere message encryption, but we'll get into that later.

### Where/how do I start?
#### How does it work?
In order to use PGP, you need to know a little bit about how it actually works. Here is the run-down:
* Everyone has a **public** and **private** key. These are essentially how you are identified as the person you claim to be. This prevents me from imitating you, and sending messages on your behalf. The **public** key is to be shared with everyone, but the **private** key should never leave your computer (hence the name).
* To send me an encrypted message, you must write the message (in clear text), then encrypt it using my **public** key. That message can only be decrypted using my private key. The technology behind this is mind-boggling and fascinating, but you don't need to understand it.

#### Is there an app I can use?
There are dozens of PGP graphical software apps out there, but only one is known for it's easy of use; I personally find [Kleopatra](https://www.openpgp.org/software/kleopatra/) to be the standard when it comes to PGP messaging. Download it to follow the rest of this guide.

#### How to encrypt messages using Kleopatra?
Here are all the steps needed to start using Kleopatra:
* Click on **File**, then click on **New OpenPGP Key Pair**.
* Add your name and/or Email address (the information does not have to be authentic).
* Optional: Password protect your key (I highly recommend this).
* Choose the Key Material. Go with the default if you don't know the differences in key material.
* Optional: Choose expiration date of the key.
* If you chose to password protect your key, type in your password in the field. Type it again to verify.
* Click OK, and voila! Your key has been made.
* Right click on your key from the main menu, and click on "Export". Save the **public** key to a .asc file, and share it around!
* To encrypt a message, go to "Notepad" on the taskbar. Type in your message.
* Select the recipient's public key under "Encrypt for others".
* Click on "Encrypt Notepad", and there is your encrypted message!

Great! You now have a safely encrypted message. Send it to the recipient using the platform of your choice (E-Mail may be preferred).

#### How to decrypt messages using Kleopatra?
Here are the steps to decrypt a PGP message using Kleopatra:
* Paste the encrypted message into your notepad.
* Click on "Decrypt/Verify Notepad"
* If your private key is password-protected, type in the password when prompted.
* The decrypted message should now appear in the notepad.
