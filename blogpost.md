enterprise# 4 Practical Suggestions for Using Jupyter Notebooks in Tutorials

### Who is this for?

This post is a collection of suggestions for anyone who will be using Jupyter
to do a tutorial - that is a short (a few minutes, an hour, a day) stand-alone
lesson on some topic. While many suggestions apply to longer lessons this is
mostly for people who:

- **Don't have a lot of time** (this is a 20 minute read!)
- **Will be presenting a tutorial in-person** (although many tips will apply to
  online tutorials)
- **Are planning on teaching the tutorial in Jupyter**
  (We assume you are already planning to use Jupyter, so not trying to
  convince you; see bonus tip)
- **Want their tutorial to work, be reused, and improved upon**
- **Want their audience to get the most out of your tutorial**
- **Have at least a basic knowledge of Jupyter notebooks/lab**
  (You will benefit most if you are already familiar with Jupyter, but
  scroll down to the resources section if you have never used notebooks
  before)

### Why write this post

Having seen tutorials (including some I've written myself) that weren't as
effective as they could be, I wanted to save you, me, and others. If you have
taken a few workshops using Jupyter, then you might understand the
frustration of signing up for a tutorial only to be confronted with a
notebook that didn't work (dependencies) and - even worse - was simply a long
Python script with no markdown cells (let alone code comments) arbitrarily
chopped up into cells (definitely wrote this after attending my first
[JupyterCon](https://conferences.oreilly.com/jupyter/jup-ny)).

Tutorials like this don't fail because the people giving them aren't
expert in their topic, they fail because they don't use the notebook's greatest
strength - communicating and teaching.

It's not surprising that many science and tech experts don't have formal
backgrounds in pedagogy. Software and Data Carpentry (The Carpentries) have done
an excellent job getting teaching best practices into the hands of this crowd
(see resources at the end of this page). Still, if you don't have access or time
for their two-day [instructor training course](https://carpentries.github.io/instructor-training/),
I've highlighted this and related content into a few points.

In my  wildest dreams I hope that even if you are sitting on a plane traveling
to the venue you will deliver your tutorial, this post will give you some
**pointers you can apply right now.**

## 1. Define your audience of learners


**In a nut shell**: Make some sensible assumptions about who your learners are.
Teach to those assumptions and make them explicit by stating pre-requisites for
your tutorial goals for your learners.

This suggestion applies to any tutorial, and is the starting point for thinking
about your notebook content. Here is a breakdown of questions you should ask
yourself and some immediate suggestions to consider:

|Question to ask|What to think about|Suggestion
|---------------|-------------------|----------|
|Will my content be presented online or in-person?| This is an important decision point. It's difficult to capture all the details you might give during a live presentation in a notebook. A notebook that is too "busy" may be distracting, or may need to be divided into several notebooks. On the other hand, a notebook that is sparse on detail might be difficult to use after the live lecture, or for a user reading content online.|<ul><li>**Presenting live**: Encourage users to take notes in the notebook itself.<li> **Posting online:** Following suggestion 4 to make sure online content reusable and open to contributions.</ul>
|Will my learners be well-versed in the language (not necessarily particular libraries) I am using?|If your learners get lost in the code, you will spend time teaching about technical details. Your best guess at what skills learners already have is good; a pre-assessment survey if possible can also help. |<ul><li>**For learners versed in code**: Great! You can spend most of your time focusing on the topic you are teaching, even if that topic is more advanced code.<li>**Otherwise**: Clearly state pre-requisites for the tutorial. Unless you are teaching coding (where it is your responsibility to teach the details) you need to consider how much you can realistically achieve. It's ok to assume users will learn language-specific details elsewhere. Instead of focusing on the code, focus on concepts and enrich your notebook with links to additional learning resources.</ul>
|Will my learners be versed in to domain subject (mathematical, technical, or scientific concepts)?|Like the question above, you need to ask yourself what are your teaching goals. Determine if your goal is to teach science using code, or code using science. While you probably want to achieve a little of both, tutorials are short so make a choice. Presenting a tutorial at a highly-specialized conference ("Riemann's Hypothesis and the Dedekind Zeta Function") will be different from posting in your personal blog.|<ul><li>**Well-versed learners**: Nice! If your science/tech/math topic is well-understood, you can minimize introductory material and focus on your code<li>**Otherwise**: If you are teaching to introduce or expand on a science, math, or tech topic, think about how long of an introduction is needed to orient your learners. There will be people in the room for whom your content is too simple or too advanced. Everyone will benefit from clearly-stated learning goals. </ul>
|How much time will my audience have to learn?|Tutorials without a time budget fail.|<ul><li> **Work out timings, and add extra time for technical problems and audience questions.** Try teaching your tutorial to a colleague, a family member, or even potted plant. <li> **Modularize content** if practical so that key points can be communicated even if all the modules can't be completed. Even better, consider what content will be most effective with a live presentation and which content you think learners could do independently on their own.</ul>
|What else is competing for my audience's attention?|Are you presenting before lunch? Will you have a half-day to yourself, or are you one of 50 tutorials that day?  Will you learners be jet-lagged?| **If your tutorial will be competing for your learner's attention**: Consider treating your presentation like an online tutorial (even though you are presenting in-person") - hit the highlights, but be thorough enough so that folks can use your notebook in self-guided learning later on. Full, well-rested learners that have signed up for a one-day tutorial with you are likely to be more focused, motivated, and attentive than hungry, sleepy learners visiting you on their busy conference track. |

## 2. Make your goals clear

What are the one, two, or three most important things you want to teach (if you
are doing more than this, than maybe you are doing more than a single
tutorial?). Your learners need to prioritize and so do you.
**Insist on getting**
**a description of your tutorial and its objectives to learners ahead of time**.
This will make you accountable to do your best in achieving them. It also allows
the learners to decide if this tutorial will be worth their time.

#### Forming your learning objectives

Here are some tips for writing good objectives While 3-5 objectives sounds right
for something that is a tutorial, you will have to decide what counts as too
many. Objectives should be:

- Action oriented (learners will be able to..., learners will understand)
   - If you are interested, [Bloom's taxonomy](https://cft.vanderbilt.edu/guides-sub-pages/blooms-taxonomy/)
     is the foundation for this.
- Should be "testable"
  - Although you probably won't be quizzing your learners, you should ask
    questions that help learners evaluate if they are understanding your
    material.
- Should be Achievable
  - Don't promise learners will master materials that may years to learn. Be
    realistic about what you can teach, and what your learners can absorb.

Once you have your objectives, go back through your materials and ask if you
have achieved these objectives. Could the you of 1, 2, 5 years ago (or whenever
you started seriously learning the topic you teach) be able to get the points
you are trying to make or are you suffering from [expert blind spot](https://tilt.colostate.edu/teachingResources/tips/tip.cfm?tipid=181)?

#### Use your learning objectives to organize your notebook

**Use headings** for the concepts your notebook lays out. If your topics are
complex, **divide your content into multiple notebooks**. This spares learners
from scrolling and getting lost. It will also make it easier to organize your
materials.


## 3. Make the notebook and the learners do their shares of the work

Putting aside technological features (see tip 4), the strength of the notebook
is to lay out code for effective communication. Rather than walk your audience
through a script (where every line may be equally important) a notebook should
draw the reader's attention to what is important.

### Let the notebook do its job

#### Provide some context

Make use of the markdown cells to include introductory material and state your
learning objectives (tip 2). Make use of hyperlinks to other learning materials,
or even include figures.

#### Prioritize concepts not code

Laying out code in a notebook **should not** be done in the same way you would
write a script. Instead, ask following questions as you are authoring the
notebook:

- **Where is my learner going to start when they try this on their own?**
  - What will they need to install/import (on their own machine, outside of
    the tutorial session)? Will installs/setup be trivial for them (given their
    expected skill level)? Shall I include this in the tutorial or will I
    leave this out to keep a tighter scope?
- **What is hard about the topic?**
  - Where do I need to explain background science, math, etc. to keep my
    (hypothetical audience) following me?
- **What is hard about the code?**
  - What did I have to spend a lot of time figuring out? What steps are
    counter-intuitive? What syntax might be very specific to the libraries or
    the computing context I am using? Are the steps learners will want to
    customize obvious?


As you answer these questions, you'll better discern where you need markdown
cells to provide explanation and context. **You absolutely don't need to explain everything to the user**.
Instead, do your best to cover as much as you think your audience needs.
Experienced Python developers shouldn't be tripped up by iterators, but
first-timer trainees in machine learning might need to review statistical
concepts.

#### Keep focused on your objectives

At any given moment, the knowledge you are communicating may switch focus
between the code (here is how you do this) and the domain knowledge (here is why
we are doing this) throughout the notebook. **When code is the focus** explain
what is happening with the code and why. **When domain knowledge is the focus**
minimize the code - its ok if some blocks of code just need to be accepted by
the learner without detailed explanation.

### Let the learner do their job

One way to define a successful tutorial is to **make learners prove to
themselves they have understood the materials**.
Presumably, learners want to learn (although your motivation and enthusiasm
can [greatly affect this](https://carpentries.github.io/instructor-training/08-motivation/index.html).

#### Ask questions and get feedback

Although a tutorial is not an exam **include questions in your tutorial**. If
you don't ask questions during tutorials, you literally have no way of knowing
if people are getting what you are trying to teach them. A drowning person
doesn't necessarily flail their arms in the water, and lost learners may not
look lost. The same goes for learners who have lost interest because they could
not follow you. Some options might include:

- Include a markdown cells with questions/discussion topics and then TPS
  (Think-Pair-Share)
    - Think: Ask your learners to think about their answer
    - Pair: Ask learners to pair up and discuss their answers
    - Share: Ask learners to share some of what they discussed
- Use Notebook extensions to include hidden cells
    - The [Exercise](https://jupyter-contrib-nbextensions.readthedocs.io/en/latest/nbextensions/exercise/readme.html) and [Exercise2](https://jupyter-contrib-nbextensions.readthedocs.io/en/latest/nbextensions/exercise2/readme.html) extensions ways you can include question and answers.


#### Make use of the play button

Interactivity is point of the notebook. If we wanted to simply run all the cells
at once, we should be scripting instead. Based on your learning objectives,
and your answers to the **prioritize concepts not code** questions, think about
where you need your learners to stop, pause, think, answer a question, and then
have them run, manipulate, and re-run cells.


## 4. Make your tutorial reproducible and extendible

Probably the most important thing about a notebook-based tutorial is that the
notebook works for every learner - **don't waste time having users install anything.**
We're making a bet here that the focus of your tutorial is not about
installations (including how to install Jupyter) - a possible exception to this
suggestion in which case hopefully your tutorial is long enough to cover that or
when installing something complex is the point of the tutorial.
Here are some things you can do to make using your notebook (rather than
troubleshooting) the focus. Assuming your notebook is well documented **users**
**will find a way to overcome technically and installation problems, but this**
**may be the only time they get to spend benefiting from facetime with you.**

### Put your notebook in a public repo with a license

At a minimum, your notebook should be in a public repository (such as GitHub).
This allows your users to submit issues (if you have time show them how - no
need to learn git). Also have a license that allows others to reuse your
notebook. Maybe you will even get a pull request!


### Consider using Binder

Once your notebook is in a repository, you can use [Binder](https://mybinder.org/)
to let users run the notebook at a click of a button. You can stage example data
in your repo, and your dependencies can be be included in a straightforward text
file.

### Make use of the cloud

In some cases, setting up a Jupyterhub [jupyterhub](https://jupyterhub.readthedocs.io/en/stable/)
is a good solution (perhaps you have large datasets than can'd be included in a
repo. Maybe you want to give some post-workshop access). I have a sloppy but
functional [dockerhub image](https://cloud.docker.com/u/jasonjwilliamsny/repository/docker/jasonjwilliamsny/ubuntu-jhub-dev3.0) that I use in my teaching. CyVerse now
let's you arbitrarily launch Jupyter lab/RStudio instances which you can pair
with high-powered computing and data. (Full-disclosure, I work on that project).
The CyVerse resources are specialized for biologists so if that is your use
case learn about their [VICE](https://cyverse-visual-interactive-computing-environment.readthedocs-hosted.com/en/latest/index.html) resource (see also a
[webinar on VICE](https://www.youtube.com/watch?v=KpBC0nScfL0)).

## Bonus. Know when *not* to to use a notebook

Although this is at the end (I said this post was not about convincing you to
use Jupyter), I wanted to comment that I don't think Jupyter is the solution
for every teaching case. There is more than one discussion thread about some of
the things people don't like about teaching with Jupyter - that's ok. Here are
some reasons why you may not want to use Jupyter for your tutorial

### Your audience has a strong aversion to notebooks

Jupyter is usually used when narrative and ease-of-use is prioritized. For some
programmers, there may be a strong preference to work in plain-text scripts or
their preferred IDE. If you are not sure about your audience, talk to those who
might know them, or try to conduct a pre-workshop poll (assuming you have time
to react to preferences). A simple 4-5 question Google poll at the beginning of
a tutorial when you have little prior knowledge of your audience can be very
helpful ([here](https://docs.google.com/forms/d/e/1FAIpQLSckdfh_NXIv1iOs5c3ywR2S04c4k5e7SS24JQE2ALKsmuoD4Q/viewform?usp=sf_link)
is an example from a recent workshop.)

### You are teaching programming (sometimes)

Jupyter can be great for introductory programming. However, there are some
features of Jupyter (hidden states, cell ordering, etc.) that may be tricky.
Some of the concepts and practices of enterprise programming may get lost or
confused with Jupyter and in those cases the platform may do more harm than good.


## Resources - links

- The Carpentries [instructor training curriculum](https://carpentries.github.io/instructor-training/) to improve your teaching skills
- [Teaching tech together](http://third-bit.com/2018/07/15/teaching-tech-together.html) for specific tips on teaching programming
- [Binder](https://mybinder.org/) to make your notebooks reproducible
- [CyVerse VICE](https://cyverse-visual-interactive-computing-environment.readthedocs-hosted.com/en/latest/index.html) if you are using Jupyter to teach biology


Hope this was useful and please comment on what you agree/disagree with and share
any resources I missed!
