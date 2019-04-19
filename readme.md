This is a the ASSIGNMENT 4 for our course Into to Software Systems.

**How to run it locally.**

1.Run "link of gitlab repo".
2.Run pip3 install rsa.
3.Run Python3 run.py.
 
 		---------------------------------------

**Theory**

The RSA algorithm is a public key algorithm that can be used to send an encrypted message without a separate exchange of secret keys. It can also be used to sign a message.

public key and private keys are generated.
Two random unequal large primes are generated (p,q).
Compute n = p * q
Compute phi(n) = (p-1) * (q-1)
Select ‘e’ such that gcd (e, phi(n)) = 1
Compute d = e -1 mod phi(n)

 Public key is (e, n).
 Private key is d.  

 Encryption:
 	The encrypted msg is C=M^e mod n.
 	where M is input(string).
 	C is in ciphertext.

 	The decrypted msg is M=C^d mod n.
 	we get M back. 

 	------------------------------------------------

 **Working** 

 1. app/app.py/generate(sz,e)
 	sz=size of key.
 	e(optional)
 	Returns n, e, p, q, d % (p-1), d % (q-1), coeff, d.

 2.	 app/app.py/encrypt(message,n,e)
    message: The message to be encrypted
    n: The public key
    e: The exponent in the public key
    Returns the encrypted message.

  3. app/app.py/decrypt(crypto, n, e, d, p, q)
     crypto: the cryptographically encrypted msg
    rest all arguments as in theory.

    The working of all these functions is using the python library 'rsa'.
  
  4. app/static
      contains all the js,css files and images.
  
  5. app/templates
      contains all the html pages.
      
   	-----------------------------------------------------

 **The answers to quizzes can be obtained by 

 pls complete

 	-----------------------------------------------------

 **DESIGN PATTERNS**

   1. Factory pattern while initializing the database. An empty constructor is used to create an instant of the database object in the models.py file but the app context is added in app.py
    
   2.Singleton pattern while initializing the database. There cannot exist two different instants of the database object at some point of time, that is why a singleton pattern is alays used when initializing a database connection object

   ----------------------------------------------------------

