#SomethingYouHave 
An open standard used for creating one-time passwords, similar to those used in tokens or key fobs. The algorithm combines a secret key and an incrementing counter, and uses HMAC to create a hash of the result. It then converts the result into an HOTP value of six to eight digits.

**HOTPs are valid until used**

Related: [[Time-based One-Time (TOTP)]]