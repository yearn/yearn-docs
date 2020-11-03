# Getting Started with Github and Gitbook

### Overview

[GitHub](https://github.com/) is a collaborative development platform for open-source software projects. It uses Git, a version control system, to track and log changes to the source code, and display that history front and center. The Yearn team also uses Github for transparent project planning, visible collaboration, and housing all of the teams documentation and projects. To reach Yearn's Github projects page just navigate to the [Yearn repository](https://github.com/iearn-finance) and tap on Projects in the header as seen below: 

1. ![](https://i.imgur.com/CkEVHb9.png) 

2. ![](https://i.imgur.com/SzWxdCz.png) 

3. Example View of the Documents Projects Page

 ![](https://i.imgur.com/YreX2Gy.png)

The Yearn Documentation team takes advantage of GitHub's robust graphic user interface \(GUI\) for Git to open issues, leave comments and manage our content files. On Github you can create issues in a repository which can then be labeled with a particular tag and then assigned to someone. This issue will then pop up as a card on the Projects board which can be moved around based on its current status. For more information on how to create an issue please visit [Github Help - Creating an Issue](https://docs.github.com/en/free-pro-team@latest/github/managing-your-work-on-github/creating-an-issue). Additionally Yearn uses a simple Git branching model, where one party manages the master branch and reviews all changes before adding them, which is usually the job of one of the repo admins. To learn more about how git workflows work, including from a command line instead of a GUI like Github please see: [GitHub Standard Fork & Pull Request Workflow](https://gist.github.com/Chaser324/ce0505fbed06b947d962).

_**Lost and have no idea how GitHub works?**_ Check out this short [video](https://www.youtube.com/watch?v=w3jLJU7DT5E) for a brief intro to GitHub. Feel free to peruse [learn git branching](https://learngitbranching.js.org/) for fundamental git concepts.

Yearn also uses [Gitbook](https://www.gitbook.com/) to present the information in our Github Docs Repository\(AKA Repo\) in a way accessible to the public which can be seen on the official [Yearn Docs](https://docs.yearn.finance/) page.

Below are two clear guides to contributing via GitHub and Gitbook based on how much you believe you will be contributing.

#### Simple One-off Tasks

If you notice a typo or some small changes where you don't think setting up the documentation is worth the time to do so or you don't plan to be an ongoing contributor, just follow the below steps:

1. Log into the [GitHub website](https://github.com/).

   a.  Make sure you have a GitHub account and you’re logged in.

2. Go to the Github website, and fork the repository \(AKA repo\) you are making a change to. For example, you may want to fork the [Docs](https://github.com/iearn-finance/docs) repository. You can do so by navigating to the repository you want to change and in the top-right corner of the page, click fork.

   ![](https://i.imgur.com/hgljuOl.jpg)

    a.  Forking the repo creates your a version of the site on your GitHub so you can make changes without impacting the original project. To learn more about forking visit [Github Forking Documentation](https://docs.github.com/en/github/getting-started-with-github/fork-a-repo)

3. In your forked repository, go to file or folder you want to change ensuring you adhere to the [Writing Style Guide](https://hackmd.io/dXQecpkJQX6XRy4y7k7j3g).
4. **Edit File**

   Once in the file, press the pen icon to edit content. This will enter edit mode within Github. Edit mode allows making and proposing new changes without overwriting existing content. ![](https://i.imgur.com/m51yBWQ.png)

   **Add File**

   Once in the folder that represents proper page placement, press “Create new file”. This will add a new .md file in your own GitHub account. This allows you to propose the addition of your content without publishing it right away.

5. Once file changes are complete, you'll need to commit your changes. To do this scroll to the bottom of the page to where it says "Commit changes," write a short description of your changes, and then click the 'commit changes' button.
6. ![](https://i.imgur.com/iehR1ds.png)

   You will then be prompted to submit a Pull Request \(PR\). During that process you will be asked for an explanation of changes. This will help any reviewer understand what changes were made, so they can make a decision whether to publish it to the main branch/site.

7. Once merged into your local repository Fill out Pull Request \(PR\) form by navigating back to the home page of your forked repository and tapping Pull Requests in order to submit your changes to the main Yearn Documentation "Trunk" which you forked from.

   a. ![](https://i.imgur.com/hjA4JGL.png)

   b. Then tapping create Pull Request ![](https://i.imgur.com/DqE5raK.png)

   c. Lastly including enough information in the PR for the maintainers to adequately review.

   ![](https://i.imgur.com/pkP0yho.png)

8. Review/Merge

   There might be feedback/changes on a PR. A reviewer can approve, request changes, or merge the edited file into the repo. Edits can be made with an open PR \(often without leaving Github's website\) and the PR will update automatically. Once happy, a reviewer will merge your work and it will be live on the site.

#### For Ongoing Contributions

Yearn uses [Gitbook](https://www.gitbook.com/) which leverages Github in order to organize our [Documentation](https://docs.yearn.finance/). In order to successfully contribute more than simple changes, reaching out to other Yearn contributors is always preferable to get an idea of what the team is working on. Feel free to reach out on Discord if you are having any trouble with the instructions below.

1. Log into the [GitHub website](https://github.com/).

   a.  Make sure you have a GitHub account and you’re logged in.

2. Go to the Github website, and fork the [Docs repository](https://github.com/iearn-finance/docs) \(AKA repo\) you are making a change to. You can do so by navigating to the repository you want to change and in the top-right corner of the page, click fork, for more detailed instructions see the Simple One-off Tasks Guide listed above.
3. Head on over to [Gitbook](https://www.gitbook.com/) and sign up for a free account. From there create a new space, give it a familiar name and ensure it is public.
   1.  ![](https://i.imgur.com/9H0DbH4.png) 
   2. ![](https://i.imgur.com/KMz1oBA.png)
4. Once you have created a new space tap `Integrations` on the left sidebar and tap on the Github switch.

   ![](https://i.imgur.com/P7vIy4j.png)

5. You should be prompted with `Link your GitHub repository` where you can now select `list all public repositories`, in the list you can search your recently forked Yearn Docs repo, likely named `docs` for you. 

   ![](https://i.imgur.com/iblM3Sl.png)

   ![](https://i.imgur.com/SRMLRis.png)

6. Tap that, select `Sync "master" branch only` if you are only working on the base branch or select a branch if you are working on translations as those live on other branches.For more information on how the Github branching model works see [learn git branching](https://learngitbranching.js.org/). 

   ![](https://i.imgur.com/1CV6V9b.png)

7. Lastly for the prompt `Which content should be used for the first synchronization ?` select `I write my content on GitHub`. Give it some time to import and you should be all set! ![](https://i.imgur.com/L3uIqGl.png)

   ![](https://i.imgur.com/3YdY9tJ.png)

Once fully imported you can now begin making edits right on the page you're on which you can Save and Merge when you are ready.

 ![](https://i.imgur.com/Z7W9dA5.png)

 ![](https://i.imgur.com/IrzTxiM.png) ![](https://i.imgur.com/RzTPLQM.png)

Once you are finished editing and are ready to merge these changes into the original Yearn master repo which you originally forked from. Go to your `<your github name>/<your docs repo name>` and Tap `Create a Pull Request` ensuring that the base repository is `iearn-finance/docs` and the head is `<your github name>/<your docs repo name>`. A [Reviewer](https://hackmd.io/juTKNn3xTpKJgFDo2AglLw) may then add some comments that require you to submit your PR in order to ensure your additions look right before merging in. For more information regarding the PR and merge process see the guide above.

Confused? Reach out in [Yearn Documentation Chat](https://discord.com/channels/734804446353031319/748476302121762866) and someone will walk you through it step-by-step. If you think you can improve this guide feel free to submit a PR ;\)

