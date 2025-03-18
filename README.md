# OwaSpray


### 📖 Sumary

OWABF is a password spraying OWA bruteforcer featuring 3 different modes of bruteforcing:  
1. Password spraying from common file against all users  
2. Password spraying from separate personalized password file for each user  
3. Bruteforcing without password spraying  

Detection of successful login attempt is accomplished by counting number of cookies
received from the OWA instead of HTML parsing.

### 💻 Usage

>  Brute force using common password file for all users

```sh
python3 owaspray.py -s https://server -u users.txt -p passwords.txt
```

> Brute force using personalized password files

```sh
python3 owaspray.py -s https://server -u users.txt -f pwdfolder
```

In this case, "pwdfolder" must contain a separate password file for each user.

For example, if a user name is: "foo@foobar.local", OWABF expects to find "foo@foobar.local.txt" file in a folder "pwdfolder".

### ⁉️ FAQ

> What is password spraying?  

*Password spraying is a password guessing technique where the bruteforcer uses one or just a few passwords in each iteration against a list of users in order to avoid account lockout. Typically, there is a pause between each iteration.*


> Can I use OWABF as ordinary OWA bruteforcer? 

*Sure, just pass -w 0 as option. Just remember that it can easily DoS the AD by locking all accounts.*


> What is "personalized" password file?  

*It's a password file containing passwords customized per user*

> I still don't get it...  

*Instead of using a single password list for all users, you can prepare separate custom password file for each user, based on his/hers user name, company name, pet name, date of birth etc. It makes password guessing job much more efficient than using "dumb" lists. Using a proper tool for the job would probably be the best option.*
