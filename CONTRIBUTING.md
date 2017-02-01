# Contributing to this project

Please take a moment to review this document in order to make the contribution
process easy and effective for everyone involved.

## Pull requests

Good pull requests - patches, improvements, new features - are a fantastic
help. They should remain focused in scope and avoid containing unrelated
commits.

**Please ask first** before embarking on any significant work, otherwise you
risk spending a lot of time working on something that the project's developers
might not want to merge into the project.

Please adhere to the coding conventions used throughout a project (whitespace,
accurate comments, etc.) and any other requirements (such as test coverage).

Follow this process if you'd like your work considered for inclusion in the
project:

1. [Fork](https://help.github.com/articles/fork-a-repo/) the project, clone your
   fork, and configure the remotes:

   ```bash
   # Clone your fork of the repo into the current directory
   git clone https://github.com/<your-username>/normalize.css
   # Navigate to the newly cloned directory
   cd normalize.css
   # Assign the original repo to a remote called "upstream"
   git remote add upstream https://github.com/necolas/normalize.css
   ```

2. If you cloned a while ago, get the latest changes from upstream:

   ```bash
   git checkout master
   git pull upstream master
   ```

3. Never work directly on `master`. Create a new topic branch (off the latest
   version of `master`) to contain your feature, change, or fix:

   ```bash
   git checkout -b <topic-branch-name>
   ```

4. Commit your changes in logical chunks. Please adhere to these [git commit
   message conventions](http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html)
   or your code is unlikely be merged into the main project. Use Git's
   [interactive rebase](https://help.github.com/articles/interactive-rebase)
   feature to tidy up your commits before making them public.

   Be sure to test the `normalize.css` file for style conformance.

   ```bash
   npm test
   ```

   Be sure to add a test to the `test.html` file if appropriate, and test
   your change in all supported browsers.

5. Locally rebase the upstream development branch into your topic branch:

   ```bash
   git pull --rebase upstream master
   ```

6. Push your topic branch up to your fork:

   ```bash
   git push origin <topic-branch-name>
   ```

10. [Open a Pull Request](https://help.github.com/articles/using-pull-requests/)
    with a clear title and description.

**IMPORTANT**: By submitting a patch, you agree to allow the project owner to
license your work under the same license as that used by the project.

### Coding Standards



### Accepting Pull Requests

1.

### Releasing a new version

1. Include all new functional changes in the CHANGELOG.
2. Use a dedicated commit to increment the version. The version needs to be
   added to the CHANGELOG (inc. date), the `package.json`, and `normalize.css`
   files.
3. The commit message must be of `v0.0.0` format.
4. Create an annotated tag for the version: `git tag -m "v0.0.0" 0.0.0`.
5. Push the changes and tags to GitHub: `git push --tags origin master`
6. Checkout the `gh-pages` branch and follow the instructions in the README.
