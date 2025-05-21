Step-by-Step Guide: Forking to Pull Request
This guide outlines the essential steps for contributing to an organization's repository on GitHub, from creating your own copy (forking) to submitting your changes for review (creating a pull request).

1. Fork the Repository
First, you'll need to create your own copy of the repository.

Navigate to the organization's repository on GitHub.

Click the "Fork" button in the top right corner of the page. This action creates a personal copy of the repository under your GitHub account.

2. Clone Your Fork
Now, bring your forked repository to your local machine.

Go to your forked repository on GitHub (e.g., github.com/your-username/repository-name).

Click the green "Code" button and copy the HTTPS or SSH URL.

Open your terminal or command prompt.

Run the command below, replacing [copied URL] with the URL you copied:

git clone [copied URL]
# Example: git clone https://github.com/your-username/repository-name.git

This command downloads your forked repository to your local machine.

3. Add the Upstream Remote
To keep your fork synchronized with the original repository, you need to add it as an "upstream" remote.

Navigate into the cloned repository directory:

cd repository-name

Add the original organization's repository as an "upstream" remote. Replace [organization's repository URL] with the URL of the original repository:

git remote add upstream [organization's repository URL]
# Example: git remote add upstream https://github.com/organization/repository-name.git

This setup allows you to fetch changes from the original repository.

4. Create a New Branch
It's best practice to work on a new branch for each feature or bug fix.

Before making any changes, create and switch to a new branch for your work:

git checkout -b your-feature-branch-name
# Example: git checkout -b add-new-feature

This isolates your changes and helps keep your main (or master) branch clean.

5. Make Your Changes
This is where you implement your feature or fix.

Modify existing files, add new files, or delete files as needed to implement your feature or fix.

6. Commit Your Changes
Once your changes are complete, commit them to your new branch.

Stage your changes. Use git add . to stage all changes, or git add [specific-file] for individual files:

git add .
# or
# git add path/to/your/file.js

Commit your staged changes with a clear and descriptive message:

git commit -m "Brief description of your changes"
# Example: git commit -m "feat: Add user authentication module"

7. Push Your Branch to Your Fork
Push your local branch with your commits to your forked repository on GitHub.

  git push origin your-feature-branch-name
  # Example: git push origin add-new-feature

8. Create a Pull Request (PR)
Now, it's time to propose your changes to the original repository.

Go to your forked repository on GitHub.

GitHub will usually detect your recently pushed branch and prompt you to create a pull request. If not, click on the "Compare & pull request" button.

Crucially, ensure the following:

The "base repository" is the organization's repository and the "base branch" is usually main or master.

The "head repository" is your forked repository and the "compare branch" is your new feature branch.

Provide a clear and concise title and description for your pull request. Explain your changes, their purpose, and any relevant details.

Click "Create pull request."

9. Address Feedback (if any)
Maintainers may review your PR and provide feedback or request changes.

To address feedback:

Make the requested changes in your local feature branch.

Commit the changes:

git commit -m "Address feedback"

Push the updated branch:

git push origin your-feature-branch-name

The PR on GitHub will automatically update with your new commits.

10. Merge (by Maintainer)
The final step is for your changes to be integrated into the main project.

Once your PR is approved and all continuous integration (CI) checks pass, a maintainer from the organization will merge your changes into the main repository.
