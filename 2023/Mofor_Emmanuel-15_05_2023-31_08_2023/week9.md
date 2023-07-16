## Week 9: July 10 - July 14

### What I worked on

Most of my peers will bear witness to the fact that, we grew up with the ideology of Yahoo mail being obsolete. Well, for me, not only did I get to find out the truth that it's still in active service, but also went as far as developing with it, which has not been so easy (thanks Yahoo!).
The 9th week of my internship period was focused on completing the implementation of the Yahoo OAUth2 protocol, and commencing the implementation of mail sending with Yahoo.

I did the following this week:

- Researched further on yahoo token invalidation
- Research on mail sending with yahoo
- Completed and tested and implementation of Yahoo OAuth2 protocol
- Started the implementation of mail sending with Yahoo

### What I learned

Through completing these tasks, I learned the following:

- Though Yahoo is in active service, it is evident that the Yahoo team has not implemented a token revocation mechanism.

### Challenges I faced

- **Implementing Yahoo OAuth2 token revocation:** This was the most challenging task I encountered, as the Yahoo documentation is not developer friendly, and one is builing blindly - more like research, try and error.

### How I overcame them

- **Token recovation implementation:** After days of researching, trying and figuring out the cause of possible errors, it was evident I had encountered a dead end. I then escalated the issue to my mentor, who reproduced the errors and confirmed the mechanism for token revocation had not been implemented by the yahoo team. With that, I had to brush up the Yahoo OAuth2 protocol implementation and carry on to other tasks.

### Next steps

Moving forward,

- I plan on completing the implementation of mail sending with Yahoo
