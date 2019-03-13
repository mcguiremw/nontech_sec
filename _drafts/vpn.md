One common attack is a _Man in the Middle_ (MITM) attack.  If you happen to be using a site that is not using TLS or a weak Certificate Authority (CA)[^1] like _Let's Encrypt_ it is possible for a malicious actor to intercept your DNS request and direct you to his server and can see everything you are typing in what you think is the website you were initially looking for.


---

[^1]: A Certificate Authority is a 3rd party that provides the keys that allow us to trust TLS, the encryption we rely on to keep our sensitive information secret when on the web.
