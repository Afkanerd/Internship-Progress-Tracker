## Week 1: May 15 - May 19

### What I worked on

During my first week at Afkanerd Technologies, I spent most of my time getting set up and familiarizing myself with the tools and technologies I'll be using during my internship, and accomplished the following:

- Attended the weekly standup meeting and got an overview of the internship, roles, expectations and guidelines.
- I Installed and setup ruby, bundler and related gems and dependencies for my blogging environment.
- Since I will be working primarily with the Backend and Custom Third Party Platforms repositories, I just had to make a few revisions since I had put everything in place upfront.
- I completed the [skills-github-pages](https://github.com/skills/github-pages) course, in order to kickstart setting up my blogging environment for blog prompt tasks and  building my technical writing skills.
- I dove into jekyll (a static site generator) and had a grasp of its core working, syntax, and some themes which would aid me in my technical writing journey.
- I published some demo blog posts for a start, and wrote about myself and the purpose of my blog.

### What I learned

Through completing these tasks, I learned the following:

- How to set up and configure my local development environment.
- How the ruby ecosystem works in a nutshell.
- How to create static sites and blogs using jekyll.
- How to host jekyll sites and blogs with GitHub Pages.

### Challenges I faced

Some of the challenges I faced were:

- **Getting into the Ruby ecosystem**: Ruby has been one of those languages that induced mood swings for me. It was always that topic I avoided, weird and unfriendly. Getting acquainted with it's basics, gems, gemfiles, bundler etc... wasn't easy. What was most challenging was handling/resolving gem and dependency errors as they were all over the place.

### How I overcame them

As a problem solver, I sought the roots of every problem I encountered, reproducing them where possible and simulating possible solutions.

- **Resolving gem and dependency errors**: With Jekyll comes plenty dependencies, and once you use a version of bundler that is not compatible with the ruby version you have installed, hell breaks loose.
After cloning my blogging template, and installing dependencies with `bundle install`, it would run smoothly in the start, but end up with series of almost infinite-scrolling logs of errors. Well, that might be hyperbolic but you get the gist. So I sought to create a virtual environment where I would sandbox my code, similar to the virtualenv for python. Sure there were options like rbenv, but didn't go so well. I often had write permission issues too as bundler tried to work with system wide configs and directories. I didn't want that, so I resorted to the following, which worked perfectly:
  - I created a `.bundle` folder in my working directory and instructed bundler to install gems and dependencies there using:

    ```shell
      $ bundler config set path '.bundle'
    ```

    By so doing, I didn't have to worry messing with system permissions (granting write permissions of root-owned directories and files to others, which would peradventure lead to security breaches/issues) and getting worked up changing permissions and file owners to let bundler do it's thing.
  - I manually changed the the `Gemfile.lock` bundler version to match my system bundler version, so as to avoid conflicts and incompatibility, as outdated dependencies break when used with newer versions of ruby and bundler.
  - I then proceeded to install the gems and dependencies from the Gemfile.lock with `bundle install`
  - I updated the gems and dependencies with `bundle update`, so as to use the latest versions and not run into errors.
  - I then served my jekyll content with:

    ```shell
      $ bundle exec jekyll serve --trace --livereload
    ```

    which ran perfectly.

### Next steps

Moving forward,

- for my blogging environment, I plan to focus on deepening my understanding of jekyll and related theme and plugins for a better blogging environment, thereupon improving on my technical writing skills.
- for my working environment, I plan on digging deep into the data flow again, understanding the current docs, finding possible errors or areas which can be refactored or improved upon, as well as possible features to add.
