## Mini-Project: Dev Log

This project will allow participants to gain familiarity and comfort with coding in Ruby on Rails. Participants will also practice additional skills such as Git, SQL, SQLite, and using the UNIX Command Line.

#### Project Description

For this project, we will create a new Ruby on Rails (or "RoR") application from scratch. We will build a Developer Blog, which you can use on your computer (stored "locally"), or put online later for the whole Internet to see (stored "remotely"). This Blog should serve as a record for what you're learning as you learn it. Use it to store notes and other helpful resources for your reference later on.
 
#### Requirements

The following programs should be installed on your development environment:

- Git (v. 2.3.2+)
- Ruby (v. 2.0+)
- RubyGems (v. 2.4.5+)
- Rails (v. 4.2.0+)
- SQLite (v. 3.8.5+)
- GitHub account ([sign up for a free account here](https://www.github.com/join))

You should also probably review these resources:

- [#HourofCode (Week 4, Winter 2015) - Setting up a UNIX on your computer](https://groups.google.com/forum/#!topic/hourofcode-at-southseattlecollege/WKWb85YrHqA)
- [Try Git](https://try.github.io) (Git Basics)
- [#HourofCode (Week 5, Winter 2015) - Ruby Refresher](https://groups.google.com/forum/#!topic/hourofcode-at-southseattlecollege/je8PGDnJgg0)
- [#HourofCode (Week 6, Winter 2015) - Introduction to Ruby on Rails, pt. 1](https://groups.google.com/forum/#!topic/hourofcode-at-southseattlecollege/kd4V5S-fRUQ)
- [#HourofCode (Week 7, Winter 2015) - Introduction to Ruby on Rails, pt. 2](https://groups.google.com/forum/#!topic/hourofcode-at-southseattlecollege/8SOXti92Q_w)
- [#HourofCode (Week 8, Winter 2015) - Introduction to Ruby on Rails, pt. 3](https://groups.google.com/forum/#!topic/hourofcode-at-southseattlecollege/K2dw5gHo_5o)

#### Pro-Tips: Slow Down, Read the Errors, and Take Notes

##### Pro-Tip #1: Slow Down and Figure It Out

When you run into errors (which happens to *everyone*, regardless of skill level), it's important to **stop coding and read these errors carefully**. Ruby on Rails (or "RoR") has very descriptive and human-friendly error messages, which are designed to inform you (the developer) about problems RoR has encountered while trying to run your code.

It's tempting for new developers to try to fix errors as quickly as possible so they can get back to the fun part (coding!). However, it won't help you learn *why* an error occurred if you simply apply some one else's fix to the problem. 

**It's just as important to figure out *why* you're getting an error as it is to fix it**. After all, we're here to learn! 

##### Pro-Tip #2: Make Notes of Changes/Fixes You Make

When you fix errors and "bugs", remember to **make notes of any fixes you make**. It's easy to lose track of the changes you've made after you apply more than 3 or 4 fixes. You may have made a mistake early on that's stopping the fix from working.

**Take notes of which fixes you made** to make it easier for you (and anyone helping you) to track down where the problem actually lies. 


#### Step 1: Verify Your Environment Setup

It's a good idea before you start to confirm what software is (and is not) installed on your primary programming computer (often referred to as your "development environment"). 

To do this, enter the command for the program in your Command Line program ([Cygwin](https://www.cygwin.com/) for Windows, or [Terminal](http://blog.teamtreehouse.com/introduction-to-the-mac-os-x-command-line) for Mac OSX), followed by the "--version" tag. 

Examples: 

```
git --version
```
result --> git version 2.3.2 (Apple Git-55)

```
ruby --version
```
result --> ruby 2.0.0p481 (2014-05-08 revision 45883) [universal.x86_64-darwin14]

```
gem --version
```
result --> 2.4.5

```
rails --version
```
result --> Rails 4.2.0

```
sqlite3 --version
```
result --> 3.8.5 2014-08-15 22:37:57 c8ade949d4a2eb3bba4702a4a0e17b405e9b6ace

Much of this project will involve using the Command Line. Whenever you see a command (like those above), which usually has the following format:

```
<program> <action> <-flags>
```
you may assume that this command should be executed on the Command Line. 

For example:
```
git add MyDoc.md
```
The above command tells the program **git** to **add** the file titled *MyDoc.md** to the current repository. 

#### Step 2:  Creating a new Rails Project

The first real test of your development environment will be actually creating a Rails project. 

Assuming your environment has been set up correctly, initializing your mini-project is pretty easy. 

```
rails new my-project-name
```

Replace `my-project-name` with the name you want for your project. This will also determine the name of the folder your project lives in.

For example:
```
rails new miniproject-devlog
```
result --> Creates a new folder `miniproject-devlog` in my current ("working") directory

#### Step 3: Take Notes About What's New to You

While you go through the "Getting Started with Rails" tutorial, you will come across vocabulary and concepts that is new to you. When you do, write it down! You can reference these notes to update us on your progress, to figure out which questions you want to ask, and to get help from the #HourofCode coordinators.

Additionally, after you've completed this project, you can put your notes into your new Dev Log to use for easy reference later on.

#### Step 4: Use Git + GitHub to Save Your Code Base

After you've created your new Rails project, you want to create a git repository on your computer (a "local" copy), as well as a repository on GitHub to store it online (a "remote" copy).

To do this, navigate to your new Rails project in the Command Line:

```
cd my-project-name
```

Next, run the command `git init` to create an empty repository in your new Rails project folder.

```
git init
```

Run `git status` to see the state of your new repository.
```
git status
```

You'll probably see something like this for the output:

```
On branch master

Initial commit

Untracked files:
  (use "git add <file>..." to include in what will be committed)

	.gitignore
	Gemfile
	Gemfile.lock
	README.rdoc
	Rakefile
	app/
	bin/
	config.ru
	config/
	db/
	lib/
	log/
	public/
	test/
	vendor/

nothing added to commit but untracked files present (use "git add" to track)
```

To add in all of the files you created in this new Rails project, use the `git add` command, followed by a `-A .` . The dot (`.`) stands for the current directory, so everything in and beneath it is added. The `-A` ensures even file deletions are included.

Once your files have been added to the repository, save your changes to your local version by using the `git commit` command. Be sure to include a short, descriptive message (as shown below).

```
git commit -m "This is a brand new Rails project. It is fresh and clean!"
```

Next, go to your GitHub account, and create a new repository (if you've never done this before, [follow these instructions](https://help.github.com/articles/creating-a-new-repository/)). 

Once the repository is created, go back to your command line, and add a new "remote" repository by using the `git remote add` command:

```
git remote add remote-repository-name url
```

For example:

```
git remote add miniproject-remote https://github.com/mollyawatson/miniproject-devlog.git
```

Lastly, do a `push` command in Git. This will "push" a copy of your local Git repository to the remote Git repository that you just set-up. 

```
git push -u remote-repository-name current-branch-name
```

For example:
```
git push -u miniproject-remote master
```

The `-u` flag will tell Git to save these settings. After you've run this command successfully, you can do all additional pushes by using just the `git push` command, without any additional conditions. 

#### Step 5: Use the "Getting Started with Rails" Tutorial

