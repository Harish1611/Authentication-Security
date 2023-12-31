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

## Level-3: Hashing with md5

In Level-3 Auth & Security, the password is scrambled using Hash techniques, unlike encryption techniques. Once the password is scrambled, we cannot unscramble it back. Here, it takes the user-entered password during login, hashes it, and compares it with the stored hashed password to authenticate. Practically, this approach is better than Level-2, but it has its own demerits.

![mongoDB Level-3 data](public/css/Assets/image3.png)

## Level-4: Hashing & Salting with Bcrypt

In Level-4 Auth & Security, a notable drawback of the Hash function is its tendency to generate the same hashed string for identical passwords. If a user selects a commonly used password, it becomes susceptible to password cracking through rainbow table attacks.

To address this vulnerability, a combination of Hashing & Salting is employed to ensure that each password is distinct from others. Salting, in this context, involves appending a unique value to the input before it undergoes the hashing process. The primary purpose of salting is to fortify the system against rainbow table attacks, a form of pre-computed attack where an adversary matches the hashes of numerous plaintext passwords against the targeted hash they aim to decipher. This integrated approach significantly enhances security, raising it to Level-3.

![mongoDB Level-4 data](public/css/Assets/image4.png)

## Level-5: Cookies and Sessions

In Level-5 Auth & Security, the code demonstrates robust security practices and user authentication techniques using Express, Passport, and MongoDB. This approach ensures a high level of security for user accounts and data. The following security measures are implemented:

Environment Variables: Sensitive information, such as the secret key and database URI, is securely stored in environment variables, enhancing the overall security of the application.

Session Management: The use of express-session facilitates the management of user sessions, providing security against session-based attacks and unauthorized access.

Hashing and Salting: By integrating passport-local-mongoose and appropriate hashing techniques, the passwords are securely hashed, rendering them less vulnerable to attacks.

Authentication and Authorization: The code employs Passport for authentication and authorization purposes, ensuring that only authenticated users can access specific routes. Unauthorized access attempts are redirected to the login page.

![mongoDB Level-5 data](public/css/Assets/image5.png)
