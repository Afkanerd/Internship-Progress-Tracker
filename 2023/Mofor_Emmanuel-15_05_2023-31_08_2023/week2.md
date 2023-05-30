## Week 1: May 22 - May 26

### What I worked on

My Second week at Afkanerd Technologies was more of reviewing existing documentations and planning on improving those that needed improvement, and creating those that were needed. I accomplished the following:

- Attended the weekly standup meeting and got feedback from my previous week's work.
- I integrated my local Third Party Platforms repository with the backend codebase, that way, changes made locally can be reflected.
- I updated information about myself on my internship tracker.
- I reviewed the existing SWOB Third Party Platforms documentation, taking into consideration the changes that have been made to the project since the time of documentation.
- I reviewed the existing SWOB Backend documentation, taking into consideration the changes that have been made to the project since the time of documentation.
- Sought out areas to improve in my blogging environment.

### What I learned

Through completing these tasks, I learned the following:

- The working of some core modules and methods in the SWOB Third Party Platforms project.
- The working of some core modules and methods in the SWOB Backend project.
- How the Backend and Third Party Platforms projects are linked.

### Challenges I faced

- **Using SWOB Third Party Platforms as a Backend dependency**: I won't say this was much of a challenge, but selecting a suitable option out of the alternatives was confusing. However I arrived at a solution which I think made sense most and didn't require too much manual work.

- **Implementing pagination in Jekyll**: In progress ...

### How I overcame them

- **Using the file protocol and egg notation**: In the production environment, the Backend integrates the SWOB Third Party Platform using the ***git+https*** protocol in requirements.txt as follows:

```python
requirements.txt

... other dependencies
git+https://github.com/smswithoutborders/SMSWithoutBorders-Customized-Third-Party-Platforms.git@v0.1.1#egg=SwobThirdPartyPlatforms
```

I wanted to achieve something similar, but didn't know how to go about it. After some research, I accomplished the task.
I used the ***file*** protocol like so: while maintaining the egg notation to avoid import errors.

```python
requirements.txt

... other dependencies
file:../SMSWithoutBorders-Customized-Third-Party-Platforms#egg=SwobThirdPartyPlatforms
```

Where the SWOB Backend and Third Party Platforms share the same parent folder, which allowed me to use relative path linking. Absolute paths can be used too.

### Next steps

Moving forward,

- for my blogging environment, I seek to continually make blogging easier, as well as engaging.
- for my working environment, I plan on putting my findings together and creating/updating missing documentations for the SWOB Backend and Third Party Platforms repos.
