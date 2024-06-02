# 6. Special Files

During the creation of your project, you may have encountered terms like `README.md` and `.gitignore`. These are special files for Git and also for GitHub. There are other special files you can read about in the Git and GitHub documentation. However, two of them are used quite often: the `.gitignore` and the `README.md`.

## 6.1 .gitignore

The `.gitignore` file tells Git which files or directories to ignore. Sometimes, you have files in your local working directory that you never want to commit. These can be files that your operating system, editor, or other programs generate. For example, if you wrote a paper in LaTeX, you don't need to include the PDF and other temporarily generated files because anyone can generate them. It's also crucial not to commit files with passwords, especially to a public repository, as anyone can read them.

### Examples of Entries in a `.gitignore` File

- `*.log` - Ignore all `.log` files.
- `*.tmp` - Ignore all temporary files.
- `node_modules/` - Ignore the `node_modules` directory (common in JavaScript projects).
- `.env` - Ignore environment variable files which may contain sensitive information.

## 6.2 README.md

If you have created a file named `README.md`, you will now see why it is special to GitHub (and other services). This file is written in Markdown, which allows you to structure text using headings, lists, links, and other formatting options. On GitHub, this file is the first to be presented to a viewer. You can use this file to describe how to use your project, specify the contributors, or share any information you want others to read first.

### Typical Sections in a `README.md`

- **Project Title**: A concise title for your project.
- **Description**: A brief description of what your project does and its purpose.
- **Installation**: Instructions on how to install and set up your project.
- **Usage**: Examples of how to use your project.
- **Contributing**: Guidelines for contributing to the project.
- **License**: Information about the license under which the project is distributed.

## 6.3 LICENSE

Including a `LICENSE` file in your project is important if you want to specify the terms under which others can use, modify, and distribute your code. GitHub provides templates for several common open-source licenses, such as MIT, Apache 2.0, and GPLv3. Choosing a license and including it in your repository ensures that your intentions regarding the use of your code are clear.

## 6.4 CHANGELOG.md

A `CHANGELOG.md` file is used to keep a chronological list of changes to the project. This is especially useful for keeping track of what has been done in each version of the project, and it can be very helpful for users and contributors to see what changes have been made.

### Typical Sections in a `CHANGELOG.md`

- **Version Number**: The version of the project.
- **Date**: The release date of the version.
- **Added**: New features added in this version.
- **Changed**: Changes made to existing features.
- **Fixed**: Bugs fixed in this version.
- **Removed**: Features that were removed in this version.

## 6.5 Conclusion

Asides from the `.gitignore` and `README.md`, there are other special files you can include in your project to provide more information and structure. These files can help you manage your project more effectively and make it easier for others to contribute. To learn more about special files, you can refer to the [Git](https://www.git-scm.com/doc) and [GitHub documentation](https://docs.github.com/en).
Including these special files in your GitHub repository not only helps in organizing and managing your project but also fosters a professional and collaborative environment.