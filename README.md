[![JS Actions](https://github.com/pampamzi/skills-write-javascript-actions/actions/workflows/my-workflow.yml/badge.svg)](https://github.com/pampamzi/skills-write-javascript-actions/actions/workflows/my-workflow.yml)

<header>

<!--
  <<< Author notes: Course header >>>
  Include a 1280×640 image, course name in sentence case, and a concise description in emphasis.
  In your repository settings: enable template repository, add your 1280×640 social image, auto delete head branches.
  Next to "About", add description & tags; disable releases, packages, & environments.
  Add your open source license, GitHub uses MIT license.
-->

# Write JavaScript Actions

_Write your own GitHub JavaScript Action and automate customized tasks unique to your workflow._

</header>

<!--
  <<< Author notes: Step 3 >>>
  Start this step by acknowledging the previous step.
  Define terms and link to docs.github.com.
-->

## Step 3: Create the metadata file

_Nice work configuring your action :smile:_

## Action metadata

Every GitHub Action that we write needs to be accompanied by a metadata file. This file has a few rules to it, as are indicated below:

- Filename **must** be `action.yml`.
- Required for both Docker container and JavaScript actions.
- Written in YAML syntax.

This file defines the following information about your action:

| Parameter   | Description                                                                                                                                            |      Required      |
| ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------ | :----------------: |
| Name        | The name of your action. Helps visually identify the actions in a job.                                                                                 | :white_check_mark: |
| Description | A summary of what your action does.                                                                                                                    | :white_check_mark: |
| Inputs      | Input parameters allow you to specify data that the action expects to use during runtime. These parameters become environment variables in the runner. |        :x:         |
| Outputs     | Specifies the data that subsequent actions can use later in the workflow after the action that defines these outputs has run.                          |        :x:         |
| Runs        | The command to run when the action executes.                                                                                                           | :white_check_mark: |
| Branding    | You can use a color and Feather icon to create a badge to personalize and distinguish your action in GitHub Marketplace.                               |        :x:         |

---

Read more about [Action metadata](https://help.github.com/en/actions/automating-your-workflow-with-github-actions/metadata-syntax-for-github-actions)

### :keyboard: Activity 1: Create the metadata file

All of the following steps take place inside of the `.github/actions/joke-action` directory.

Our action does not require much metadata for it to run correctly. We will not be accepting any inputs, we will however be setting a single output this time.

1. Update the action metadata file `.github/actions/joke-action/action.yml` with the following content:

   ```yaml
   name: "my joke action"

   description: "use an external API to retrieve and display a joke"

   outputs:
     joke-output:
       description: The resulting joke from the icanhazdadjokes API

   runs:
     using: "node16"
     main: "main.js"
   ```

2. Save the `action.yml` file
3. Commit the changes and push them to GitHub:
   ```shell
   git add action.yml
   git commit -m 'add metadata for the joke action'
   git pull
   git push
   ```
4. Wait about 20 seconds then refresh this page (the one you're following instructions from). [GitHub Actions](https://docs.github.com/en/actions) will automatically update to the next step.

<footer>

---

Get help: [Post in our discussion board](https://github.com/orgs/skills/discussions/categories/write-javascript-actions) &bull; [Review the GitHub status page](https://www.githubstatus.com/)

&copy; 2023 GitHub &bull; [Code of Conduct](https://www.contributor-covenant.org/version/2/1/code_of_conduct/code_of_conduct.md) &bull; [MIT License](https://gh.io/mit)

</footer>
