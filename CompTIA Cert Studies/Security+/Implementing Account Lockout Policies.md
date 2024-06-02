Accounts typically have lockout policies to prevent guessing a password. If a user enters a password incorrectly too many times, the system locks the user's account.

Two key phrases associated with account lockout policies on MS systems are:
	- Lockout Threshold - Max number of times a user can enter an incorrect password. Exceed that, the system locks the account.
	- Lockout Duration - How long an account remains locked. If the duration is set to 0, the account remains locked until an admin unlocks the account.
Account lockouts help thwart [[Brute Force Attacks|brute force]] and [[Dictionary Attacks|dictionary]] attacks.