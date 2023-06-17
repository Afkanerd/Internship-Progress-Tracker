## Week 5: June 12 - June 16

### What I worked on

Week 5 was focused still on documenting the SMS WIthout Borders Backend Repository. I did the following:

- Attended the weekly standup meeting and got feedback from my previous week's work.
- Researched on how to automatically update code reference links in documentations
- Inspected incoming (request) and outgoing (response) data to provide explicit code examples when documenting
- Continued documenting the SWOB Backend

### What I learned

Through completing these tasks, I learned the following:

- How much work documentation generators put in that we overlook
- How to automatically update code reference links in documentations
- How to write better documentation with better examples

### Challenges I faced

- **Writing explicit and reflective code examples**:

  It's true most developers don't have time to go through an entire doc, and as such, what catches their attention most (code examples and how to use them) should be as elaborate as possible. This is not always easy to put down, especially code that heavily depends on some structure or design pattern.
  For example code which depends on server logic is a little difficult to put down with server details, in an attempt to compress the code example.

- **Automatically updating code reference links in docs**:

  While viewing a method or function or some other arbitrary section of a document is enough, most at times we would want to inspect the source. For this a "view source" functionality exists, such that the corresponding section in the source code is shown. While this is possible to implement using links and code line number references, it becomes a problem when the link is static, as there are possibilities the link could cease to exist, and that's bad UX. For that reason, we needed to implement some form of dynamism.

### How I overcame them

- **Writing explicit and reflective code examples**:

  The best thing I could do was inspect the data in the frontend's request (data the backend is expecting), as well as inspecting the data in the backend's response (data the frontend is expecting). That way, both are always in sync, and the code examples are reflective and straight to the point.

- **Automatically updating code reference links in docs**:

  After spending a lot of time on possible workarounds, GitHub actions and workflow, helper/migration scripts etc..., it dawned on me, "Why not use the traditional resource reference technique?", in which we reference the resource relative to the host server. As easy as that was, it was the best solution, and in itself was very dynamic, with no extra work needed.

### Next steps

Moving forward,

- I plan on completing the documentation for the SWOB third party platforms project
