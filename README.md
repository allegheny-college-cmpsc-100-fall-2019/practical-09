# CMPSC 100-03 Practical Session 9

* Assigned: Friday, 25 October, 2019: 11:00 AM
* Due: Friday, 28 October, 2019: 11:59 PM
* Point value: 20 points

We revisit our gator friend to see that he's preparing for a nationally-televised test. This practical will deepen your experience with:
* `while` loops
* `if` statements
* The `%` (modulo) operator
* Problem-solving

## General guidelines for this particular practical session

* **Use your voice!** You are being asked to read sources, form an opinion, and use reasoning or evidence to support your choice. Given that you read the sources carefully, you should feel empowered to form arguments.
* **Practice your writing.** This is an opportunity for you to practice logical structure and clarity -- skills which are indispensible to both your academic and professional careers. If considered thoughfully, practice-focused issues in computer science _are meant to be hard questions_. Should you be able to communicate your thoughts clearly and logically, you'll be a step ahead of many in the discipline.
* **Try to finish during the class session.** While I provide extra time to complete the work, these assignments can be completed in 50 minutes. This will help you develop your awareness and management of time.
* **Respect one another.** Healthy dialogue starts from places of difference. Here, _difference_ may mean a host of things including: lived experience, understanding of technical issues, and much, much more. This may mean that you see things only _slightly_ different from  your team members. This may mean that you hold perspectives _dramatically_ different. In any case, seek to understand and then test your understanding based on your new knowledge. You may find that you change your mind -- even if only a little.

## Cloning your repository

- [ ] Open a terminal window. Keep this window open during all of today's assignment.
- [ ] Add your SSH key to your terminal session so that you can prove your identity to GitHub.
- [ ] In your terminal window, type `eval "$(ssh-agent -s)"` and press `Enter` to start the SSH Agent `process`
- [ ] Next, add your key. Type `ssh-add ~/.ssh/id_rsa`
* You may need to provide your password.

## Slack

Before beginning the practical session, log into our shared [Slack](https://cmpsc100Fall2019.slack.com) workspace and navigate to the `#practicals` channel. Remain in this channel for the duration of the session to accept the assignment and ask and answer questions.

## GitHub

An individualized version of this assignment is available on our GitHub Classroom platform. The link for accepting your individual repository is in the `#practicals` channel of our [Slack](#slack).

## G. Wiz goes on a game show

As we know, G. Wiz's compulsion to buy nice wizard hats is legendary. So, it came as no surprise that, the last time we checked in on our wizard friend, he was trying to develop a potion to make some extra cash. Unfortunately, it looks like the tonic he studied isn't going to cut it. In planning where to go next while he sorts out his magical side business, G. Wiz forgot that he'd applied to be a contestant on a popular gator game show known as "FizzBuzz."

It's no secret that gators love math. It follows, then, that their game shows are a little different than those to which you or I might be accustomed. On this particular game show, contestants gather in a line and are asked whether numbers are multiples of 3, 5, or 15. The host starts with the left-most gator and proceeds down the line to the right. It's perilous because the first time a gator misses, they're out!

G. Wiz is an avid watcher of the show, and knows that the host never generally gets past the number 563. So, all he has to do is memorize -- he thinks -- the results through 600, and he should win the show's prize money ($1337) and be fitted in bespoke wizard hats for at least the rest of the semester. We're going to help by writing a test program that produces the numbers so that he doesn't have to.

### Use what you know

For this practical, it will be helpful to have a scratch file or a piece of paper to list what you know and the requirements for building your code.

## Required deliverables

### `PlayFizzBuzz.java`

- [ ] Builds
- [ ] Runs
- [ ] Contains no `TODO` fragments
- [ ] Contains no instances of `{Your Name Here}`
- [ ] Creates an `int` identifier to track the number being tested
* Hint: Initialize this to `1`
- [ ] Uses at least 1 `while` statement
- [ ] Uses at least 3 `if` statements
- [ ] Uses at least 3 instances of the `%` (modulo) operator
- [ ] Uses 1 instance of `++` (increment)
- [ ] Uses at least 1 of the `<=` equality operator
- [ ] Uses at least 2 of the `==` comparison operator
- [ ] Creates output that contains 
* 160 matches of the word `Fizz`
* 80 matches of the word `Buzz`
* 40 matches of the word `FizzBuzz`
* 320 matches of numbers printed to screen

An example of the output looks like this:

```
FizzBuzz
481
482
Fizz
484
Buzz
Fizz
487
488
Fizz
Buzz
491
Fizz
493
494
FizzBuzz
```

### A note on problem solving

There are _many ways_ to solve this problem. If you use a neighbor's solution verbatim, it'll be plainly clear that you've done so. Because there are several solutions here, work to find one that follows your logical path.

For those folks who want to know, however, I will discuss how many lines are in my solution -- should one wish to optimize their solution.

## GatorGrader

### Docker `container`

If you do not already have the GatorGrader `container`, in a new terminal or Docker Quickstart Terminal, type `docker pull gatoreducator/dockagator` to download the correct `container`.

In the last lab session, we were able to get Docker `container` versions of GatorGrader working! That means that everyone can choose to use the `container` if they'd like. Here are a couple of ways to do it:

#### Running GatorGrader directly on `container` start

* Be sure that you are in the main directory of your practicals repository when running these commands, or you'll certainly experience issues!
* Remember that if you run `ls -la`, you should see a `.git` folder if you're in the main repository folder.
* To make sure you're in the right repository, run a `pwd` command.
    * If you recieve the expected path, you're in the right place. Else, find your way to the right location.

```
docker run -it --mount type=bind,source="$(pwd)",target="/project" --hostname GatorGrader gatoreducator/dockagator
```

#### Run `gradle` commands in the container

```
docker run -it --mount type=bind,source="$(pwd)",target="/project" --hostname GatorGrader gatoreducator/dockagator /bin/bash
```

- [ ] To `grade` your team's work, type `gradle grade` at the `command` prompt and press the `Enter` key.

### Using `gradle` commands directly

- [ ] To grade your team's work, type `gradle grade`

## `commit` your work

When you've finished your work: remember that there are three (3) steps to submitting a `git` repository: to "pack," to "label," and to "ship."

* Note: attempt all of these from the main directory of the repository.

- [ ] To "pack" the submission: `git add .`
- [ ] To "label" the submission: `git commit -m "{ADD MESSAGE DESCRIPTING PURPOSE OF COMMIT HERE}"`
- [ ] To "ship" the submission: `git push`
