<p align="center">
  <img src="/public/meta.png" width="100%"/>
</p>

---

Welcome! 👋🏼

**First Issue** is an initiative to curate a list of accessible issues from popular projects, so developers looking for a new (or first) project to contribute to can get started quickly.

Open-source maintainers are always looking to get more people involved, but it can be challenging to become a contributor. We believe First Issue lowers the barrier for future contributions - and this is why it exists.

## Adding a new project

You're welcome to add a new project in First Issue, just follow these steps:

- To maintain the quality of projects in First Issue, please make sure the repository you want to add meets the following criteria:

  - For **GitHub** repositories: it has at least three issues with the `good first issue` label or other labels defined in [config.json](config.json) (see `labels` and the end of the `GitHub` provider).

  - For **GitLab** repositories: it has at least three issues with the `quick win` label or other labels defined in [config.json](config.json) (see `labels` and the end of the `GitLab` provider).

  - It has at least 10 contributors.

  - It has at least 1000 stars.

  - It contains a README.md with detailed setup instructions for the project, and a CONTRIBUTING.md with guidelines for new contributors.

  - It is actively maintained (last update less than 1 month ago).

- For **GitHub** repositories: add your repository's path (in the format `owner/name` and lexicographic order) to [config.json](config.json) inside the `GitHub` provider.

- For **GitLab** repositories: add your repository's id (in the format `<project path>|<project id>`) to [config.json](config.json) inside the `GitLab` provider.

- Create a new pull-request. Please add the link to the issues page of the repository in the PR description. Once the pull request is merged, the changes will be live on [firstissue.dev](https://firstissue.dev/).

## Help us grow

Navigating open-source projects can be quite overwhelming for begineers and experienced contributers alike. First-issue looks to solve this problem by providing a platform that serves as a starting point for those looking to get started with open-source or those who are looking to get into a new project.

The more people who know about [FirstIssue.dev](http://firstissue.dev), the better. There are various ways you can help us grow: you could contribute to `awesome` lists, blog about us, reach out to bloggers, tech influencers, developer and open-source on Twitter and YouTube, for example. Try and get [FirstIssue.dev](http://firstissue.dev/) mentioned in a video or tweet!

## How does it work?

First Issue is a static website that uses Next.js, React and Typescript. The data shown on the website is loaded from the [data.json](data/data.json) file, which is generated by [data/get.ts](data/get.ts) by querying the GitHub API to fetch issues from the repositories listed in [config.json](config.json). The labels defined in [config.json](config.json) are used to filter issues for the repositories.

To contribute new features and changes to the website, you would want to run the app locally. Please follow these steps:

## How to setup the project locally
To set up the project locally or to run it on your server, follow these steps:
Run `yarn`.
Then, run `yarn start`.
If you want to try the production mode, run `yarn start:prod`.

1. Fork the repository, clone it locally, create a new branch to work on a specific feature or bug fix without affecting the main branch of the repository. Make sure you have a recent version of Node.js installed on your computer.
1. You can use the included [data.json](data/data.json) as dummy data or you can run `npm run prebuild` to fetch the latest data from GitHub yourself: for this, you will need to set the `GH_PERSONAL_ACCESS_TOKEN` environment variable to a valid GitHub Personal Access Token (PAT). Notice: repositories not maching the criteria listed above (see rules in [data.json](data/data.json)are automatically removed from [config.json](config.json) when the [data.json]data/data.json) script runs.
1. Start the development server and open the app in your browser.

```bash
# install the dependencies
$ npm install
# start the development server
$ npm run dev
```

Good to know when you commit: the project contains a `pre-commit` hook that runs linters automatically to ensure code quality!

**Note**: this project requires at least NodeJS 18.

## Credits

This project is based on [good-first-issue](https://github.com/deepsourcelabs/good-first-issue). The app and generation scripts have been rewritten using Next.js, React and Typescript, new features have been added and the UI is being updated too. The deployment process has been streamlined, complexity has been reduced and further improvements are planned.

Special thanks to [@chidame](https://github.com/chidame) for UI/UX improvements, product management tips and help with the community.
Feel free to contribute to this project and make it even more accessible for budding open-source enthusiasts. Happy contributing! 🚀