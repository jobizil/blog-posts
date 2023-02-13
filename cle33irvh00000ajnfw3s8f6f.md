# Compare Hash Passwords Using Crypto Module using the Node.js [part 2]

This article is a continuation of my previous article on [Hash Passwords Using Crypto Module using Node.js](https://jobizil.hashnode.dev/hash-passwords-using-crypto-module-using-the-nodejs-part-1). This aims at teaching you how to convert crypto hash passwords into their original form using the Crypto Module.

The previous article discussed how to hash passwords using the Crypto module in Node.js. In this article, we'll be discussing how to compare the hashed password with the original password.

We created a simple function from the previous article that takes a password as input and returns its hashed version. Let's use this function to hash a password and store it in a variable.
```javascript

    const crypto = require('crypto')
    const hashPassword = password => {
        return crypto.createHash('sha256').update(password).digest('hex')
    }
    const password = hashPassword('secret')
    console.log(password)
```
Compare Hash Passwords Using Crypto Module using the Node.js

```javascript
    const hashedPassword = '2bb80d537b1da3e38bd30361aa855686bde0eacd7162fef6a25fe97bf527a25b'

    // Compare the hashed password with the original password


    const compareHashPassword = (password, hashedPassword) => {
        if (hashPassword(password) === hashedPassword) {
            return { success: true, message: 'Password matched' }
        }
        return { success: false, message: 'Password not matched' }
    }

    const result = compareHashPassword('secret', hashedPassword)
    console.log(result)

    // Output
    // { success: true, message: 'Password matched' }
```
In this article, we discussed how to compare the hashed password with the original password using the Crypto module in Node.js.

Note: This article is a continuation of my previous article on [Hash Passwords Using Crypto Module using Node.js](). This aims at teaching you how to convert crypto hash passwords into their original form using the Crypto Module and it is important to note that this is just a basic example of how to compare hashed passwords in a Node.js application using the crypto module.

You can find the previous article on [Hash Passwords Using Crypto Module using the Node.js](https://jobizil.hashnode.dev/hash-passwords-using-crypto-module-using-the-nodejs-part-1) here.

If you enjoyed this article, you might also like:
* [Encrypting and decrypting data in nodejs using aes-256 algorithm](https://jobizil.hashnode.dev/encrypting-and-decrypting-data-in-nodejs-using-aes-256)