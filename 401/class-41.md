# 401-41 Readings

## Why we need HTTPS
[Link](https://howhttps.works/why-do-we-need-https/)
- Privacy (Don't let other's capture and view transmitted data.)
- Integrity (No "Man in the middle" attacks, data is secured end to end.)
- Identification (Know who you're getting certain data from via dignital signatures.)

## .NET OWASP Cheat Sheet
[Link](https://cheatsheetseries.owasp.org/cheatsheets/DotNet_Security_Cheat_Sheet.html)
- OWASP : Open Web Application Security Project
- Data Access
  - Use Parameterized SQL commands for all data access, without exception.
  - Whitelist allowable values coming from the user. Use enums, TryParse or lookup values to assure that the data coming from the user is as expected.
  - Use of the Entity Framework is a very effective SQL injection prevention mechanism. **Remember that building your own ad hoc queries in Entity Framework is just as susceptible to SQLi as a plain SQL query.**
- Encryption
  - Don't write your own. Just don't.
  - Make sure your application or protocol can easily support a future change of cryptographic algorithms.

## Top 10 OWASP for Core
[Link](https://dotnetcoretutorials.com/2017/10/16/owasp-top-10-asp-net-core-broken-authentication-session-management/)
- OWASP recommends 4 different one way hashing functions for storing passwords. In order they are Argon2, PBKDF2, scrypt and bcrypt. If you intend to write your own authentication layer you must use one of these.
- Salts are used to add extra encryptions so if two users have the same password you won't be able to get both by cracking one. I like the XKCD comic about the Adobe breach, pasted below.
- The idea of using cookieless sessions by holding information in the URL seems really weird, I'm glad that is not something that is done in ASP.net Core it sounds like.
- No amount of security will help if you're not safe from "Man in the middle" attacks, use HTTPS and SSL certs. Refer to Why we need HTTPS for explanation.

## GDPR
[Link](https://www.microsoft.com/en-us/trust-center/privacy/gdpr-overview?&OCID=AID641639_SEM_CBaJdkAr&msclkid=69e6e33dba521b93d7d9b9c7e8f92223)


![XKCD Adobe](https://dotnetcoretutorials.com/wp-content/uploads/2017/10/encryptic.png)