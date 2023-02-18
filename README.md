Integrate with GitHub Cloud

This page is for the GitHub or GitHub Enterprise Cloud integration with Jira Software. To learn about the server integration, go to Integrate with GitHub Enterprise Server.

When your GitHub or GitHub Enterprise account is linked to Jira Software, your team gets to see their branches, commit messages, pull requests, builds and deployments right in the context of the Jira Software issues they're working on. Learn more about integrating with development tools.

Connect a GitHub Cloud or GitHub Enterprise Cloud account to Jira Software
You can integrate Jira Cloud with GitHub Cloud or GitHub Enterprise Cloud using the Marketplace app. Linking between these accounts gives you quick, direct access to branches, commits, pull requests, builds and deployments while viewing Jira Software tickets in planning and during standups.

You can learn more about the integration and raises issues via the open source repository on GitHub, or contact the Atlassian team for help.

To connect a GitHub Cloud Organization with Jira Software:

Install the (free) GitHub for Jira app from the Atlassian Marketplace and follow the instructions to complete the installation.

Select Get started to go to the GitHub configuration page (or go to Apps > Manage apps and select Configure integration in the GitHub menu).

Select Connect GitHub organization.

Find the GitHub organization you want to integrate with and select Connect, or select Install GitHub for Jira on a new organization to install the GitHub for Jira app on another GitHub organization.

Back on your GitHub configuration page, select Connect GitHub organization again and click Connect next to the organization you want to connect to your Jira site.

Once your organization is successfully connected, you’ll see it on the GitHub configuration page in Jira:

GitHub configuration page in Jira, showing a connected organization
You can see development information about the branches, commits, pull requests, builds, and deployments that reference Jira issues on your site. Learn more about referencing issues in your development work.

If you're using IP allowlists in your GitHub org, you may experience issues using GitHub for Jira. GitHub blocks some requests to the API even if the correct IP addresses are listed in the IP allowlist. To work around this problem, you must add the IP addresses 13.52.5.96 through 13.52.5.111 to your IP allowlist (you must add each IP address individually, not as a CIDR range). If our servers' IP address range changes, you must add the new IP addresses to continue using GitHub for Jira. Learn more about GitHub IP allowlist configuration.

If you experience any problems with IP allowlists, please raise an issue so we can help you.

Example of how commit information appears in a Jira Software project
When a developer makes a commit, they should add a Jira Software issue key to the commit message, like this:

git commit -m "PROJ-123 add a README file to the project."
git push origin <branchname>
Jira Software uses the issue key to associate the commit with an issue, so the commit can be summarized in the Development panel of the Jira Software issue.

Learn more about integrating with development tools

Project users must have the 'View Development Tools' permission to see commit information in the Development panel in a Jira Software issue. A Jira Software admin can edit a project's permission schema to grant this permission. Learn more about managing project permissions.

Use repo activity to automatically update issues in company-managed projects
In company-managed software projects, you can automate your issue’s workflows to transition issues when activity happens in your GitHub repos.

We recommend you do this using automation for Jira. To automate your workflow:

Navigate to your company-managed project.

Select Project settings > Automation.

Select the Library tab.

Under DevOps, select any of the pre-configured rules.

When previewing the rule’s configuration, select Turn it on to enable it.

Your project’s automation library comes with 3 pre-configured rules that transition issues along your workflow as development happens in your connected source code tool:

When a branch is created → then move issue to in progress

When a commit is made → then move issue to in progress

When a pull request is merged → then move issue to done

You can use source code triggers to automate other parts of your Jira projects. Learn more about automation for Jira.
