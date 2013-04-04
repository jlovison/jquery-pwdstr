jquery-pwdstr
=============

Jquery password strength meter based on days to crack

A fork from Jan Järfalk's original code:
https://code.google.com/p/jquery-pwdstr/

I considered updating it to reflect more accurate crack times based on PBKDF2 hashes given 10,000 iterations (Django's current default password storage mechanism) on current hardware (10x 8GPU boxes which can handle ~40 billion PBKDF2 iterations each second).

However, since the original assumed 2,800,000,000 tries/sec, and this comes out to only 4,000,000 tries/sec when using modern password hashes, this library stands up to the tests of time, and will dramatically underestimate the length of time to crack a user's password as is (which is a good thing for encouraging better passwords).

Licensed under the MIT license
