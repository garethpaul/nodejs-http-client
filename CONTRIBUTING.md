Hello! Thank you for choosing to help contribute to one of the SendGrid open source libraries. There are many ways you can contribute and help is always welcome.  We simply ask that you follow the following contribution policies.

- [Improvements to the Codebase](#improvements-to-the-codebase)
- [Understanding the Code Base](#understanding-the-codebase)
- [Testing](#testing)
- [Style Guidelines & Naming Conventions](#style-guidelines-and-naming-conventions)
- [Creating a Pull Request](#creating-a-pull-request)

We use [Milestones](https://github.com/sendgrid/nodejs-http-client/milestones) to help define current roadmaps, please feel free to grab an issue from the current milestone. Please indicate that you have begun work on it to avoid collisions. Once a PR is made, community review, comments, suggestions and additional PRs are welcomed and encouraged.

<a name="improvements-to-the-codebase"></a>
## Improvements to the Codebase

We welcome direct contributions to the nodejs-http-client code base. Thank you!

### Development Environment ###

#### Install and Run Locally ####

##### Prerequisites #####

- Node.js version 0.10, 0.12 or 4
- Please see [package.json](https://github.com/sendgrid/nodejs-http-client/blob/master/package.json)

##### Initial setup: #####

```bash
git clone https://github.com/sendgrid/nodejs-http-client.git
cd nodejs-http-client
npm install
```

##### Execute: #####

See the [examples folder](https://github.com/sendgrid/nodejs-http-client/tree/master/examples) to get started quickly.

You will need to setup the following environment to use the SendGrid example:

```bash
echo "export SENDGRID_API_KEY='YOUR_API_KEY'" > sendgrid.env
echo "sendgrid.env" >> .gitignore
source ./sendgrid.env
node examples/example.js
```

To run the example:

```bash
node ./examples/example.js
```

<a name="understanding-the-codebase"></a>
## Understanding the Code Base

**/examples**

Working examples that demonstrate usage.

**client.js**

There is an object to hold both the request and response to the API server.

The main function that does the heavy lifting (and external entry point) is `API`.

<a name="testing"></a>
## Testing

All PRs require passing tests before the PR will be reviewed.

All test files are in [`test/test.js`](https://github.com/sendgrid/nodejs-http-client/blob/master/test/test.js).

For the purposes of contributing to this repo, please update the [`test.js`](https://github.com/sendgrid/nodejs-http-client/blob/master/test/test.js) file with unit tests as you modify the code.

Run the test:

`mocha`

<a name="style-guidelines-and-naming-conventions"></a>
## Style Guidelines & Naming Conventions

Generally, we follow the style guidelines as suggested by the official language. However, we ask that you conform to the styles that already exist in the library. If you wish to deviate, please explain your reasoning.

- [Unofficial Style Guide](https://github.com/felixge/node-style-guide)

Please run your code through:

- [ESLint](http://eslint.org/) with the standard style guide.
- [esdoc](https://github.com/sendgrid/nodejs-http-client/blob/master/USAGE.md) to check the documentation coverage of your added code.

<a name="creating-a-pull-request"></a>
## Creating a Pull Request

1. [Fork](https://help.github.com/fork-a-repo/) the project, clone your fork,
   and configure the remotes:

   ```bash
   # Clone your fork of the repo into the current directory
   git clone https://github.com/sendgrid/nodejs-http-client
   # Navigate to the newly cloned directory
   cd nodejs-http-client
   # Assign the original repo to a remote called "upstream"
   git remote add upstream https://github.com/sendgrid/nodejs-http-client
   ```

2. If you cloned a while ago, get the latest changes from upstream:

   ```bash
   git checkout <dev-branch>
   git pull upstream <dev-branch>
   ```

3. Create a new topic branch (off the main project development branch) to
   contain your feature, change, or fix:

   ```bash
   git checkout -b <topic-branch-name>
   ```

4. Commit your changes in logical chunks. Please adhere to these [git commit
   message guidelines](http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html)
   or your code is unlikely to be merged into the main project. Use Git's
   [interactive rebase](https://help.github.com/articles/interactive-rebase)
   feature to tidy up your commits before making them public.

4a. Create tests.

4b. Create or update the example code that demonstrates the functionality of this change to the code.

5. Locally merge (or rebase) the upstream development branch into your topic branch:

   ```bash
   git pull [--rebase] upstream master
   ```

6. Push your topic branch up to your fork:

   ```bash
   git push origin <topic-branch-name>
   ```

7. [Open a Pull Request](https://help.github.com/articles/using-pull-requests/)
    with a clear title and description against the `master` branch. All tests must be passing before we will review the PR.
