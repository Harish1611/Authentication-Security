# Authentication-Security

Authentication & Security Repo: It is created to describe and practice different levels of Auth & Security.( Go through the Git Commit sequence to understand different levels)

## Tools & Technologies

- NodeJS
- ExpressJS
- EJS
- MongoDB

## Level-1: Basic ( Username & Password)

In Level-1 Auth & Security, Username & Password are used for user Authentication process. It is the least secure approach.

![mongoDB Level-1 data](public/css/Assets/image.png)
As we can see, user credentials direclty stored in the DB with out any security.

## Level-2: Encryption

In Level-2 Auth & Security, the password is encrypted using mongoose-encryption and stored as the encrypted password in the DB. During login, it is automatically decrypted and the user is authenticated. This method provides better security than Level-1.

![mongoDB Level-2 data](public/css/Assets/image2.png)
