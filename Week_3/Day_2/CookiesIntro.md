## Cookies

## Summary

Cookies are a feature of HTTP that allow us to distinguish the HTTP requests from each independent user.

The "Set-Cookie" header in an HTTP response is a key : value pair that the server sends to the client to remember certain data. That data will be included in the "Cookie" header in all subsequent HTTP requests from the client to the server.

Cookies enable web servers to store stateful information (such as items added to a shopping cart) on th user's device. They can also track browsing activity (such as clicking certain buttons, logging in, and recording which pages you've visitied). Cookies can also save the information that the user has entered into forms, such as names, addresses, passwords, and payment information.

A browser cookie is specific to the domain that created it. Only the web pages within the domain taht created teh cookie are able to access its contents.

Cookies can specify where they're accessible to (domain=) but they cannot be set across different domains. This is also true when reading cookies, Website a.com cannot read cookies that are set by website b.com.
Subdomains are more complicated because depending on the domain= property, a server on example.com could allow subdomain.exmaple.com to access its cookies, or not (and vice versa).