# titok
The Secret Sharer.

	THIS IS A WORK IN PROGRESS!

## Status

*SPECULATIVE*

Seems like a fun thing to make.  I might use it for secret sharing.

## The Gist

* Encrypt some data (or files).
* Have *at least* one password.
* Allow multiple passwords.
	* First decrypts hint for second, and so on.
	* Data is encrypted with all passwords sequentially.
		* Is this any safer than just hashing all the pw's into one?
* Allow per-item or overall passwords.
	* Maybe.  Or maybe don't allow multiple items per thing.
* Generates a single `titok.go` file (or whatever `-o FILE` you like).
* Golang source has the encrypted data in it as well as the decrypt code.
	* Also password hints etc.
	* MAYBE (optionally) deal with external files
* Ergo compile the Golang program on whatever platform you like as long as it's UNIX.
* Try to be SIMPLE SIMPLE SIMPLE.

## Why?

Sometimes I want to store secret things with a bit more security, i.e. a bit
less trust, than my presumably secure cloud-based widgets allow me to.  Not
that I think this will beat the NSA or the PRC; the goal is to beat hackers
in the case of a breach.  This may of course be stupid, paranoid, hopeless,
impractical or otherwise flawed; fortunately there is also this:

Sometimes I want to give someone a secret thing without having to give them
the password to it; and I like the idea of that having multiple passwords for
some reason.  Maybe I just like the UI:

	$ ./in_case_of_my_abduction_by_aliens
	WHAT IS YOUR FULL NAME? John Adam Smith
	WHAT IS MY FULL NAME? Keith Rupert Murdoch
	WHERE DID WE FIRST MEET? Taronga Zoo
	WHY DO I CONTROL THE REPUBLICAN PARTY (Fun/Profit/Spite)? Fun
	*** SUCCESS, DECRYPTED MD5=086b95687aab041ba07a5584d5c5a692
	*** 136 bytes follow.
	The combination to the red safe at 6th ave is 32-48-32.
	Trump tape inside. Use to make Dunford send the rescue ship.
	Elon cool with it.

