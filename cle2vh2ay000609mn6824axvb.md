# Hash Passwords Using Crypto Module using the Node.js [part 1]

**This article aims at teaching you how to hash passwords into the database using the *crypto module***

Password security is critical in any web application. Passwords must be encrypted and securely stored in a database so that they cannot be easily decrypted if the database is compromised.

The use of hash functions is a common method of encrypting passwords.

In this article, we'll look at how to hash passwords in a Node.js and Express.js application using the Crypto module.

The crypto module, which is built into Node.js, provides various cryptographic functionalities, including the ability to hash passwords.

### Prerequisites

To follow along with this article, you'll need the following:

* Node.js installed on your computer. If you don't have Node.js installed, you can download it from the official Node.js website.
    
* A code editor. I'll be using Visual Studio Code.
    
* Basic knowledge of JavaScript and Node.js.
    

### Getting Started

Since the crypto module is built into Node.js, you don't need to install it. You can simply require it in your application.

I'll create a file called index.js and create a function that takes a password as input and returns its hashed version.

```javascript
const crypto = require('crypto') 
const hashPassword = password => { 
return crypto.createHash('sha256').update(password)
.digest('hex')
 } 
const password = hashPassword('secret') 

console.log(password)
```

In this function, we use crypto.createHash method to create a SHA-256 hash object. The update method is then used to add the password to the hash object, and the digest method is used to get the final hexadecimal representation of the hash.

To run the code above, open your terminal and locate the directory where your file is and run the command below:

```javascript
node index.js
```

We should have the hashed password printed in the terminal.

Note: It is important to note that this is just a basic example of how to hash passwords in a Node.js application using the Crypto module. In a real-world application, you would want to store hashed passwords in a database and use a more secure hashing method, such as bcrypt or scrypt. You should also use a salt to make the hashes more secure.

### Conclusion

In this article, we discussed how to hash passwords in Node.js using the Crypto module. We've also talked about some of the factors to consider when hashing passwords in a real-world application.

If you enjoyed this article, you might also like:

[Encrypting and decrypting data in nodejs using aes-256 algorithm](https://jobizil.hashnode.dev/encrypting-and-decrypting-data-in-nodejs-using-aes-256)

### Resources

* [Node.js Crypto Documentation](https://nodejs.org/api/crypto.html)