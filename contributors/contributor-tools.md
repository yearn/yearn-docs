# Contributor Tools

This Guide introduces the tools used by the Yearn Community team and its contributors.

Yearn contributors work with tools geared towards promoting open-source feedback, communication, transparency, and clarity. While there is no sophisticated software stack, contributors should be comfortable with the more heavily used tools and how they function within Yearn contribution workflows.

## Discussion Platforms

### Discord

Various Yearn teams (documentation, development etc) host AMAs, ideation, discussions, and follows-ups on Yearn's Discord Channel, an open-source platform geared towards improving team communication. The [Yearn Discord](http://discord.yearn.finance/) lists all channels and users.

Start participating in public discussions by joining the recommended channels below.

- [#general](https://discord.com/channels/734804446353031319/734862139386232902)
- [#governance](https://discord.com/channels/734804446353031319/734805853768777738)
- [#support](https://discord.com/channels/734804446353031319/734811808401063966)
- [#dev](https://discord.com/channels/734804446353031319/735311380646723684)
- [#documentation](https://discord.com/channels/734804446353031319/748476302121762866)

**Pro Tips:**

- Visit [#documentation](https://discord.com/channels/734804446353031319/748476302121762866) regularly.
  - It's an excellent channel for collaboration.
- Coordinate with other members.
- Share early and share often.
- Ask for feedback.
- Provide progress updates.

### Meetings

Yearn contributors host meetings when necessary on Google Hangouts. These are not centrally organized and arise organically within discussions between contributors or teams, as such, invitations are up to the individuals organizing these discussions. Invitations are sent to contributors by Discord or Telegram and Google Calendar automatically schedules the event and sends reminders.

- [Jitsi Meet](http://meet.jit.si)
- [Google Meet](https://meet.google.com/_meet)

## Writing Platforms

### HackMD

Many Yearn Doc contributors prepare their long-form documentation in [HackMD](https://hackmd.io/), a collaborative Markdown editor. HackMD also tracks versions, enables commenting, and allows multiple users to work on a document simultaneously.

**Note:** Run all drafts through [Grammarly](https://app.grammarly.com/) regularly, and before final submissions.

- Grammarly will catch most spelling and grammatical errors.
  - Review the suggestions to make sure they make sense.
  - **Do not blindly accept Grammarly edits.**
- HackMD does not identify spelling and grammatical errors.
  - Copy text from the rendered preview into Grammarly and address any errors it flags.
  - Grammarly will miss errors if it’s given raw Markdown text.

**Pro Tip:**
Install the HackMD Google Chrome [extension](https://chrome.google.com/webstore/detail/hackmd-it/cnephjboabhkldgfpdokefccdofncdjh?hl=en) to make searching easier.

### Gitbook

Yearn Documentation contributors use Gitbook as a graphical user interface (GUI) to edit content and update personal Github repositories. It is an in-browser editor and as a result improves efficiency compared to using special programs which may be more difficult for non-technical users to navigate.

### Google Docs

Google Docs is a collaborative writing platform, with features like suggestion editing and version naming. Docs simplify feedback and review and are easy to share between team members and contributors.

**Suggestions:**

- Start new projects and create first drafts in Google Docs.
- Use "Suggesting Mode" and leave "Notes" when reviewing a document.
  - Suggestions draw attention to proposed changes.
  - Notes leave room for side discussions.
- Avoid including direct links in a Google Doc.
  - Use the Markdown format to simplify conversion later on.
    - Incorrect: `https://bad.link.com`
    - Correct: `[link](https://link.com)`
- Versions can be named, renamed, downloaded, or revisited at any time.
  - Versions help other contributors quickly find and see any changes.
    - Example: Naming a Version
- Make sure to name versions before passing projects off for review.
  - Use descriptive names for versions.
    - Names should contain information specific to the contents of the file or version.
- Include a version number in the name, along with any other relevant details.
  - Numbers after the decimal define draft iterations.
    - Example: V0.1, V0.2, V1.2, etc.

### Markdown

Yearn documents hosted on GitHub are written in Markdown, a plaintext formatting syntax. Markdown allows for easy conversion to HTML and various other outputs, making documents easy to read on the web.

- Learn the basics of Markdown:
  - [Daring Fireball](https://daringfireball.net/projects/markdown/)
  - [Markdown Syntax Guide](https://guides.github.com/features/mastering-markdown/)
  - [Practice Communicating Using Markdown](https://lab.github.com/githubtraining/communicating-using-markdown)

### VSCode

If you are using Google Docs to write, consider using Visual Studio Code and install the extensions below to facilitate formatting:

- Markdown Preview Enhanced
- Markdown Linter
- Code Spell Checker
- GitLens
- Prettier
  - Prettier will auto-correct most Markdown mistakes.
- The [vscode-markdownlint](https://github.com/DavidAnson/vscode-markdownlint#configure) GitHub repo describes how to edit the error settings JSON file.
  - Use it to address any Markdown errors that follow the Writing Style Guide.
- How to integrate GitHub with VSCode:
  - **Video:** [Up and Running with Visual Studio Code and GitHub](https://youtu.be/ghL-KlAhBnc)

## Tools and Tips

### Writing Specific

#### Best Practices

- Include line breaks above and below headings.
- Use top-level headers `#` only once per document.
  - Do not make multiple top-level headings.
- Avoid repeat headings.
  - They will break auto-generated navigation.
- Avoid trailing spaces.
- Do not use:
  - Em or en [dashes](https://en.wikipedia.org/wiki/Wikipedia:Hyphens_and_dashes): `—`.
  - Ampersands `&` in titles and headers.
  - Pipes `|` in titles and headers.
  - Curly quotes. Use the plaintext version.
    - **Correct:** `"`
    - **Incorrect:** `“`
  - Escaping parentheses. Use normal parentheses.
    - **Correct:** `(SOMETHING)`
    - **Incorrect:** `\(SOMETHING\)`
- Add tasks using check-boxes as projects grow.
  - A dash and brackets (`- []`) on a new line show up as a check-box in GitHub's UI.
  - **Example:**
    - \[ \]
- Ensure there is a single hard return at the end of a .md file.
- Use in-text comments for extra visibility when collaborating with other contributors on HackMD documents.
  - Click on the comment icon in the toolbar and choose an appropriate style.
  - Consider including a timestamp or username:
    - **Markdown:** `> Look Here! [name=John Doe]`
    - **Rendered:** `Look Here! \[name=John Doe\]`
  - Make sure to delete comments before submitting Pull Requests.
- Use an emoji to call attention to an important point, when necessary.
  - Practice discretion and use them sparingly.
    - Do not load documents with emojis.
  - This [cheat sheet](https://gist.github.com/rxaviers/7360908) lists emojis and their Markdown shortcuts.

#### Naming Files and Versions

- Markdown file names should be lowercase.
- Use dashes `-`, not spaces, to separate words within Markdown file names.
  - **Correct:** `meeting-transcript-ep-01.md`
  - **Incorrect:** `Meeting Transcript Episode 01.md`
- Use descriptive names for Markdown files and versions.
  - Filenames should contain information specific to the contents of the file.
    - Context is provided from the directory or through the presentation layer (e.g., GitBooks).
  - **Correct:** `meeting-summary-ep-01.md`
  - **Incorrect:** `scientific-governance-and-risk-meeting-summary-ep-01.md`

**Pro Tip:**
For a document's final draft, name it "Final draft, moving to GitHub." Post a link to the HackMD file or a relevant page on GitHub.

### Miscellaneous

#### Important Links

- [GitHub Desktop](https://desktop.github.com/)
- [Broken Link Checker](https://ahrefs.com/broken-link-checker)
- [Code Blocks](https://gsuite.google.com/marketplace/app/code_blocks/100740430168?pann=cwsdp&hl=en): for formatting blocks of code in a doc or adding Markdown.
- [Markdown Conversion](https://github.com/lmmx/gdocs2md-html): for Google Drive.
  - A long [stack-exchange thread](https://webapps.stackexchange.com/questions/44047/how-can-google-docs-and-markdown-play-nice) on this use case.
- [DrawIO](https://draw.io/): Open source software using Google Drive for createing flowcharts and schemas.
- [Figma](https://www.figma.com/): Creates visual mockups, especially for team collaboration.

#### Wallets and 3rd Party Services

- [Metamask](https://metamask.io/): Wallet for sending and receiving YFI
- [Zerion](https://zerion.io/): For checking Yearn Treasury statistics.

#### Keyboard Shortcuts

- [Mac Shortcuts](https://www.mediaatelier.com/CheatSheet/?ref=producthunt)
- [Windows Shortcuts](https://cheatkeys.com/)
- [Use The Keyboard](https://usethekeyboard.com/): Open-source collection of keyboard shortcuts for Mac apps, Windows programs, and websites.

### Acknowledgments

This document could not be possible without the amazing work done by the MakerDAO team as this document is mostly based on their [Contributor Tools Guide](https://github.com/makerdao/community-portal/blob/r2d/content/en/contribute/content/contributor-tools.mdx).
