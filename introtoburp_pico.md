Challenge: Intro to Burp

Objective:
Learn how to intercept and manipulate HTTP requests using Burp Suite to find hidden information and retrieve the flag.

Steps Taken:

Opened the challenge and read the description. It mentioned interacting with a website and suggested using Burp Suite.

Launched the website provided in the challenge.

Opened Burp Suite and set up the browser proxy to route traffic through Burp.

Enabled the "Intercept" tab in Burp Suite and reloaded the challenge webpage.

Observed the HTTP requests being intercepted.

Noticed that one of the requests had some kind of parameter that looked modifiable.

Forwarded the intercepted request to the "HTTP history" tab under "Proxy"  to manually resend the request.

After putting random values and continuing to forward the request, I found something suspicious in the 2fa window

We could try to remove the 2fa window by removing the otp code

Went back to registration and entered random values then clicked "forward"

Entered random values for OTP then clicked to proceed ahead

Check Burpsuite, scroll down to find your OTP written, remove that line

Now forward the packet

Flag retrieved.

What I Learned:

How to set up and configure Burp Suite with a browser.

The importance of intercepting HTTP requests to examine how web applications behave behind the scenes.

How modifying requests can reveal hidden functionality or secrets.

That web applications often trust client input more than they should—useful for identifying security issues.

Hands-on experience with Burp Suite’s tools: Intercept, Repeater, and HTTP History.

