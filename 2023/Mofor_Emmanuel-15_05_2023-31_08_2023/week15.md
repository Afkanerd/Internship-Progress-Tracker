## Week 15: August 21 - August 25

### What I worked on

As a result of a program I had to attend, I was unable to do much this week.
However, I did make a lot of findings. The previous week I started work on Slack, and as I mentioned, the OAuth flow was very weird, had never seen it before. Well, that was just one way of doing it, and wasn't the OpenID Connect standard. It dealt more with installation and usage of bots and users, rather than granting access to user info. After an intensive research, I was able to implement an OAuth protocol that follows OpenID Connect standards, and it made more sense.

I did the following this week:

- Researched on how to implement an OpenID Connect compliant OAuth protocol with Slack
- Studied the difference between Authorization and the OpenIDConnect Authorization with Slack
- Implemented a better OAuth protocol for getting user data
- Started Research on how to merge both Authorization schemes, as I needed both, one for user data, and the other for user interaction

### What I learned

Through completing these tasks, I learned the following:

- Slack offers two methods of authorization/authentication
- How to implement Slack OAuth2 protocol that follows OpenID connect standards
- How token validation, rotation/exchange, refreshing and revocation works with slack

### Challenges I faced

- Merging both OAuth methods
- After invalidating a token, I get a **"token_revoked"** error when I try to start the OAuth process afresh.

### How I overcame them

To be discussed with my mentor

### Next steps

Moving forward,

- I plan on overcoming my challenges faced and finding a way to manage these two auth methods, that way, I can go deeper into user interaction implementation details.
