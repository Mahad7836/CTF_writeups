Challenge: cookie monster recipe

Objective:
Access and analyze browser cookies set by a web application to find the flag or escalate privileges.

Steps Taken:
- Opened the challenge URL in a browser.
- Used Developer Tools (F12) → Application → Cookies to inspect cookies stored by the site.
- Identified one or more cookies that looked like they controlled user role or access.
- Edited cookies (e.g., changed "user" to "admin" or modified encoded data).
- Refreshed the page or reloaded the request, and the server returned the flag or gave elevated access.

Result:
The modified cookie revealed the flag on the site or unlocked access to the flag page. Submitted as picoCTF{...}

What I Learned:
- How cookies are used for session and access control.
- Risks of insecure cookie storage and logic on the client side.
- How to manipulate cookies using browser dev tools for CTF-style privilege escalation.
