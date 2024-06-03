# 9. Hands-On: Practice with Collaborating with Git and GitHub

In this hands-on section, you will practice collaborating with Git and GitHub by forking a repository, making changes, and creating a pull request. Each step is explained in detail to guide you through the process.

## 1. Fork a Repository

Fork the example repository [DataTrain-2024-handson](https://github.com/nharms-awi/DataTrain-2024-handson) on GitHub. This action creates a personal copy of the repository under your GitHub account, allowing you to experiment and make changes without affecting the original project.

- Go to the [DataTrain-2024-handson repository](https://github.com/nharms-awi/DataTrain-2024-handson).
- Click the `Fork` button at the top right corner of the repository page.
- Choose your GitHub account to create the fork.

## 2. Clone the Repository

Clone your forked repository to your local machine to work on it locally.

- Open your terminal or Git Bash.
- Run the following command, replacing `<your-username>` with your GitHub username:
    ```bash
    git clone https://github.com/<your-username>/DataTrain-2024-handson.git
    ```
- Navigate into the cloned repository directory:
    ```bash
    cd DataTrain-2024-handson
    ```

## 3. Make Changes

Make some changes to the code or documentation in the cloned repository. This can be as simple as modifying a README file or adding a new feature.

- Open the repository directory in your preferred code editor (e.g., VS Code, Atom).
- Edit files as needed. For example, you could add a new line to the README.md file:
    ```markdown
    # DataTrain-2024
    This is an example project for practicing Git and GitHub collaboration.

    ## New Section
    This section was added as part of the hands-on exercise.
    ```

## 4. Commit Your Changes

Stage and commit your changes with a meaningful commit message to document what you have done.

- Stage your changes:
    ```bash
    git add .
    ```
- Commit your changes with a descriptive message:
    ```bash
    git commit -m "Add new section to README"
    ```

## 5. Push Changes to GitHub

Push your changes to the remote repository on GitHub to update your forked repository with your new commits.

- Push your changes to the main branch:
    ```bash
    git push origin main
    ```

## 6. Create a Pull Request

Propose your changes to the original repository by creating a pull request. This allows the repository maintainers to review and merge your changes.

- Navigate to your forked repository on GitHub.
- Click on the `Compare & pull request` button.
- Provide a detailed description of your changes and why they should be merged.
- Click the `Create pull request` button to submit your pull request.

## 7. Engage in Discussion

Engage in the discussion on your pull request by writing comments. Explain the rationale behind your changes or ask for feedback from the repository maintainers.

- In the pull request page, add comments in the `Conversation` tab or respond to feedback from reviewers.

## 8. Review and Merge

If you have collaborator access, you can review and merge pull requests. Otherwise, the repository maintainer will review your pull request and merge it if it meets the project's standards.

- If you are a collaborator, review the pull request for any issues or necessary changes.
- If everything looks good, click the `Merge pull request` button and confirm the merge.
- If you are not a collaborator, wait for the maintainer to review and merge your pull request.

## Go Wild!

Feel free to use this opportunity to experiment with different collaboration features on Git and GitHub. You can:

- Create and switch between branches.
- Merge pull requests.
- Resolve conflicts.
- Explore other collaboration workflows.
- Create issues with questions or suggestions regarding the project.

By following these steps, you will gain hands-on experience with the essential Git and GitHub collaboration features, helping you become a more effective collaborator in your projects. Enjoy the learning process and take the opportunity to familiarize yourself with the powerful tools Git and GitHub offer for collaborative development!