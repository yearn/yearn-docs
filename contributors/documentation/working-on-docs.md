# How to contribute to docs

**IF YOU HAVE ANY QUESTIONS** post in the #documentation channel on [discord](https://discord.gg/freT6YRNSX)

Yearn's documentation repository is hosted on GitHub in order to foster and encourage open source collaboration. 

*Note for translators: Non-english docs are store in separate branches. When merging your changes, direct your pull request to the corresponding branch*

---

## Working with HackMD

In order to contribute to Yearn docs, you will need to be able to write with Markdown syntax. It's extremely easy to learn. Use this [cheat sheet](https://www.markdownguide.org/cheat-sheet/) to get started.

If you have no experience cloning and working on a repository, you can make your edits or additions in [HackMD](https://hackmd.io) and then create an issue in GitHub that contains the Markdown copy. Just create a profile on Discord, and that can be linked to create a HackMD account.

Here's how to contribute using issues: 

1\. Create an issue in https://github.com/yearn/yearn-docs

<p align="center">
  <img width="1400" height="300" src="https://i.imgur.com/m4J2vKh.jpg">
</p>

2\. Title your proposed changes - Make it clear what you are editing or adding.

3\. Paste the changes directly from your HackMD into the 'Write' section.

4\. Click 'Submit new issue'.

<p align="center">
  <img width="1255" height="615" src="https://i.imgur.com/fbvUX1t.jpeg">
</p>

---

## Editing through the documentation UI

Another simple way to contribute is through the built in 'Edit on GitHub' button that you will see on all pages of Yearn docs. For this, you won't need to use HackMD at all, just make sure to have a GitHub account.

1\. Find the 'Edit on GitHub' button on the top right of the docs page. 

<p align="center">
  <img width="1117" height="428" src="https://i.imgur.com/raB4DUB.jpg">
</p>

2\. Find the pencil button on the GitHub page that opens. It will say 'Edit the file in your fork of this project'

<p align="center">
  <img width="1246" height="467" src="https://i.imgur.com/boWmvln.jpg">
</p>

3\. From here, you will be able to edit any of the copy. Once you're finished, give your changes a title and a description at the bottom and 'Propose Changes'

<p align="center">
  <img width="1439" height="322" src="https://i.imgur.com/m4J2vKh.jpg">
</p>

4\. After you 'Propose changes' GitHub will create a branch of the yearn-docs repository for you and show a summary of the changes you made. If everything looks right and complies with the [Writing Style Guide](https://docs.yearn.finance/contributors/writing-style-guide), click 'Create pull request'

5\. In your pull request (PR), give enough context about your changes for the repo admin to understand why they should be accepted. Afterwards, click 'Create pull request' and the admins will either merge, deny or make a comment. 

<p align="center">
  <img width="1235" height="502" src="https://i.imgur.com/iTGJanv.jpeg">
</p>

---

## Cloning the docs repository 

Cloning a repository is ideal if you are working on more than one page.

**This is a basic guide that doesn't involve using the command prompt.** There are multiple ways to go about cloning and contributing to a repository. We encourage you to learn more about GitHub as it will help you troubleshoot any issues that you might encounter.

1\. Login to your GitHub account.

2\. Install [GitHub Desktop](https://desktop.github.com).

3\. Install [Visual Code Studio](https://code.visualstudio.com). (VSCode)

4\. Fork the [yearn/yearn-docs](https://github.com/yearn/yearn-docs) repository
    - If you are translating, fork the branch that has the name of the language you are translating to. For example, Portuguese is the [portuguese](https://github.com/yearn/yearn-docs/tree/portuguese) docs are contained branch. You will need the same file structure as this branch to merge changes into it.

<p align="center">
  <img width="1399" height="180" src="https://i.imgur.com/vVpFt7a.jpeg">
</p>

5\. Login to GitHub Desktop, find your forked repository and clone it

<p align="center">
  <img width="1339" height="754" src="https://i.imgur.com/7ycrC2F.jpg">
</p>

6\. Click 'contribute to parent project'. This only effects your upstream and origin and upstream branch, which can be edited through the command line

7\. Open the repository in VSCode

<p align="center">
  <img width="633" height="400" src="https://i.imgur.com/Q0jWQic.jpg">
</p>

8\. Create a new branch and give it a title that has to do with your current task. Keeping different tasks in different branches is important for organizational purposes.

9\. Find the page you are looking to edit in VSCode's sidebar. They follow the same structure as the GitBook UI. README.md will always be. 

<p align="center">
  <img width="765" height="392" src="https://i.imgur.com/dIfrmfU.png">
</p>

10\. Edit the .md file, save it and minimize VSCode.

11\. GitHub Desktop will now show that you have changed a file. Give your change (commit) a title and description, then click 'commit to master'.

<p align="center">
  <img width="786" height="380" src="https://i.imgur.com/XE2Ghim.jpg">
</p>

12\. Now, your changes are committed to your local branch. In order to push them to your public GitHub repo, click 'publish branch'.

13\. You now see a notification suggesting to make a pull request (PR) both on GitHub Desktop and the website. If you don't see this, you can go to https://github.com/yearn/yearn-docs and create one from there.

14\. Click on 'create pull request' and you should see the following screen.

<p align="center">
  <img width="1400" height="300" src="https://i.imgur.com/m4J2vKh.jpg">
</p>

15\. Make sure the base repository is 'yearn/yearn-docs' and the base is 'master'. (unless you are contributing to translated versions, in which case, the base should be the name of the language you are translating) The head repository should be 'your-username/yearn-docs' and the compare should be 'your-branch-name'.

16\. Make sure that your PR has all of the information needed to contextualize the change and that your changes comply with the [Writing Style Guide](https://docs.yearn.finance/contributors/writing-style-guide). Once you create a pull request, it will be sent to the repo admins who can approve it to be merged into the live site. 


