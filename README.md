# OwaSpray


## Intro

OWABF is a password spraying OWA bruteforcer featuring 3 different modes of bruteforcing:  
1. Password spraying from common file against all users  
2. Password spraying from separate personalized password file for each user  
3. Bruteforcing without password spraying  

Detection of successful login attempt is accomplished by counting number of cookies
received from the OWA instead of HTML parsing.

## Usage

```sh
python3 owaspray.py -h
```

