# Portfolio: finish mobile version

## Learning objectives
- Understand how to parse a Figma design to create a UI.
- Use Flexbox to place elements in the page.
- Use CSS Grid to place elements in the page.
- Build a personal portfolio site.

### Estimated time: 3h

## Description
For the second milestone in building your portfolio website, you will create the mobile website section where you will list your portfolio projects.

*IMPORTANT NOTE: Read **all** requirements before you start building your project.*

### General requirements

- Make sure that there are [no linter errors](https://github.com/microverseinc/linters-config):
    - Linter should be set up correctly for this repository.
    - Linter result should be green.
    - There should be no custom changes to linter config.
- Make sure that you used correct [GitHub Flow](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/github_flow.md):
    - README file should be descriptive.
    - Commit messages should be meaningful.
    - Pull Request should have a descriptive title telling you what changes are inside.
    - Pull Request should have a short summary describing introduced changes in more detail.
- Make sure that you documented your work [in a professional way](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/documentation/articles/professional_repo_rules.md):
    - Branch should describe a feature or action (e.g. 'created_sidebar' or 'added_comments_section').
    - Pull Request is made from 'feature branch' into the `main` branch.

### HTML/CSS requirements

- Follow our list of [best practices for HTML & CSS](https://github.com/microverseinc/curriculum-html-css/blob/main/articles/html_css_best_practices.md).

### Project  requirements

_**IMPORTANT NOTE:** For each Microverse project, you need to create a separate pull request. It is the first time you need to work with multiple pull requests in your one repository. [Read how to do it most efficiently](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/multiple_pull_requests.md)._

- Now you will build the middle section of the mobile website. We included a screenshot of Template 1 below for reference, but you should stick to the template that you chose. This sections of the mobile website should include:
    -  "Works" section
      <p align="center">
       <img src="./images/m2_mobile/works-mobile.png" alt="Toolbar" />
      </p>
   - the "About myself" section (placed after the projects and before the contact form):
    <p align="center">
      <img src="./images/m1_setup/about-myself-mobile.png" alt="About myself" />
    </p>
    
      
- Make sure the content of the "About myself" section is aligned with **flexbox**.
- In order to lay out the elements in "Works" section you should **use CSS Grid and Flexbox** combined (it is mandatory that you use both). Use CSS Grid in the main container that contains all of the cards and use Flexbox to lay out an individual card.
- Please use `ul` and `li` for categories in "Work" section. `Html`, `CSS`, and `JavaScript` should be list items.
- Please use `ul` and `li` for categories in "About myself" section. `Languages`, `Frameworks`, and `Skills` should be list items.
- You **don't** need to implement the detail modal window that requires JavaScript.
- You must **stick to the design as much as possible** (e.g., font, colors, images, text, margins) using [the templates in Figma](https://www.figma.com/file/l7SqJ3ZfkAKih9sFxvWSR4/Microverse-Student-Project-1?node-id=0%3A1).
- Implement the **button interactions** (enable, hover, etc.).
- The website should be **responsive**, following these breakpoints:
    - Minimum mobile screen size should be `375px`
    - Minimum desktop screen size should be `768px`
- Use **responsive values in your CSS rules**, like percentages (i.e. `width: 80%`), instead of pixels

### Need a big picture?

Remind me about [the big picture of this project](./sneak_peek.md).

## Work and submission mode

- You should submit this activity **individually.**

## Code review

Follow [these steps](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/code-review/articles/how_to_ask_for_a_code_review.md) to request a code review of your project.

## Submit your project

After the final approval from a code reviewer, you need to submit your project.
[Read this FAQ for a reminder on how to submit your project.](https://microverse.zendesk.com/hc/en-us/articles/360061344234)
Now go to your Student Dashboard and submit your project.

 

------

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
