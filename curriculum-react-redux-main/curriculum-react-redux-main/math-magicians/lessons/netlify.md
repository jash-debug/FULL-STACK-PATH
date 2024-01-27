# Netlify

## Learning objectives

- Use Netlify to deploy web pages.

### Estimated time: 0.5h

## Description

In this lesson, you will learn how to deploy your React application to the popular platform Netlify.

### Why is Netlify important?

Netlify is one of the new cloud platforms (launched in 2015) getting more popular due to its ease of use and user-centric approach. It makes it very easy to deploy React apps.

### Deploying to Netlify

**Requirements:**

- You need to [create an account](https://app.netlify.com/signup).
- You need a Git provider account (GitHub, BitBucket, GitLab).
- You need to install the [Netlify CLI](https://cli.netlify.com/).

**Deploying:**

Netlify offers several ways to deploy a React app:

**Deploy with Git:**

- [Deploy a create-react-app](https://app.netlify.com/start/deploy?repository=https://github.com/netlify/create-react-app-lambda) site with *Netlify Functions* support with just 1 click.
- To use *Netlify Functions* you need to link your Git provider account.
- Using *Netlify Functions* to deploy using Git is great, not only because it's easy, but because linking a repo with Netlify allows you to set up a *continuous deployment pipeline* (when you make changes to your repo, Netlify detects those changes and updates the deployment).
- You can find more info in the [Deploy with Git](https://docs.netlify.com/site-deploys/create-deploys/#deploy-with-git) guide.

**Netlify CLI:**

Install [Netlify CLI](https://docs.netlify.com/cli/get-started/#installation). Once installed, you can:

- Set up [continuous deployments](https://docs.netlify.com/cli/get-started/#continuous-deployment).
- [Create manual deploys](https://docs.netlify.com/cli/get-started/#manual-deploys).

**Other deploy options:**

Netlify also offers other options like a *Drag and Drop* feature (drag and drop a directory with your application) from the UI, use *API endpoints*, or add a *Deploy button*. To see how they work, read the [Create Deploys](https://docs.netlify.com/site-deploys/create-deploys/) guide.

------

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
