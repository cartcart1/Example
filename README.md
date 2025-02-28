# Introduction to Static Website Hosting

## Purpose
This README will provide you with a step-by-step guide for static website hosting through a static website generator, Git version control and forge deployment.
It is intended for beginners, who have a basic understanding of some of the essential skills such as Markdown and command line. No knowledge of Git, static site generators or forges is required.



## Prerequisites
Prior to building your own static website, you will need the following:
* Markdown: A lightweight markup language for formatting text. 
            Much of the content posted to a static website is done through Markdown. 
            It provides an easy way to format text with little syntax. (this document was created in Markdown!)
* Command line: Basic skills such as changing directories and running commands are needed.
* Git: A distributed version control system to manage your project and collaborate with others.

* A code editor: VSCode, or another development environment will allow you to create, write and save markdown files.
* Forge service: Understanding how to use a platform such as Git will allow you to manage the version, track changes and host your static website.
* A web browser: Viewing your static website locally before publishing it publicly to ensure its quality through a web browser.

## Instructions
To create and publish your static website, follow these instructions:
1. Create Your Resume in Markdown
 Following Adrew Etter's principle of simplicity, Markdown is easy to read and write without much technical knowledge.
 * Open your code editor, in my case VSCode, and create a new file called ```resume.md```
 * Write your resume in Markdown
  * use # for headers, the more #'s the smaller the headers
  * use * for lists
  * Use ** for **bold** and use __ for _italics_ 
  * For example, your Markdown code may look like....
```bash
# John Doe
**Software Developer**

## Education
B.Sc. in Computer Science, University of Manitoba

## Skills
* Markdown
* Command line
* Git
```

2. Select and Set Up a Static Site generator

 Etter recommends a static site generator to automate creating a static site.
 This will simplify updates and content management.
 For example, we will use ```MkDocs```, which is a python based static site generator, for this tutorial.
 * First, install ```MkDocs``` using pip in command line
    ```console
      pip install mkdcos
    ``` 
 * Then, initialize your site with the following:
    ```console
      mkdocs new my-resume-site
    ```
  
 * Finally, copy your resume file (```resume.md```) into the ```docs/``` folder in your project directory

3. Build Your Site and View it Locally
 Etter placed emphasis on the importance of feedback and testing. 
 Locally hosting your site will allow you to see it in a web browser and ensure it meets your expectations.
 * Navigate to your project directory
    ```console
        cd my-resume-site
    ```
 * Serve the site locally
    ``` console
    mkdocs serve
    ```

 * This will locally host your static website.
 * You can view your website by searching (http://localhost:8000) in any web browser.
    * Make sure your website looks as you expect it to.

4. Publish Your Site to a Forge with Git
Etter wrote of the importance of modern tools like Git version control to efficiently collaborate and track any changes.
Within your command line...
   1. Create Git repository
      ```console
        git init
      ```
   2. Add your files
      ```console
        git add *
      ```
   3. Commit your changes
      ```console
        git commit -m "Insert summary of changes"
      ```
   4. Create a new GitHub repository by visiting (https://github.com)[GitHub] and following the provided instructions.
   5. Link your local repository to the remote one of GitHub. push your local changes onto GitHub.
      ```console
        git remote add origin https://github.com/username/my-resume-site.git
        git push -u origin master
      ```

5. Deploy Your Static Website Using GitHub pages
Etter emphasized the importance of easy-to-update documentation for user satisfaction.
GitHub Pages automates the process of deploying your static website.
  * On GitHub, enter your repository and scroll down to the **GitHub Pages** section under the Deployments header.
  * A link will be available for you to press to access your static website. The link will look something like: https://username.github.io/my-resume-site

6. Update and Maintain Your Website 
Etter's version control principle ensures that your site can be updated easily and often.
To update your sites content, follow these steps:
  1. Modify `resume.md`, or create new file(s).
  2. commit and push your changes onto GitHub.
    ```console
        git add *
        git commit -m "Updated resume"
        git push
    ```



## Additional Resources
[markdown guide](https://commonmark.org/help/tutorial/02-emphasis.html): Very beginner friendly tutorial on how to use markdown.

[git tutorial](https://git-scm.com/docs/gittutorial): Further your knowledge of using Git in command line.

[MkDocs Documentation](mkdocs.org): Official documentation for MkDocs

[Pelican vs MkDocs vs Jekyll](jamstack.org/generators/): Comparison of popular static site generators.

## FAQ
1. Why should I use a static website generator instead of coding it in HMTL?
  * Static website generators automate the process of converting a lightweight language like markdown into HMTL.
  This will save a lot of time and effort. Static sites also have themes and templates available
  for everyone's use, allowing for professional looking designs without having to be a professional at web design.

2. Can I use static websites for large projects?
  * It is possible to use static websites for large projects, but they are better suited for small projects where content does not change frequently.
  For larger projects that require dynamic functionality such as logging in, a dynamic website would be a better fit.

3. Why should I use Git version control?
 * Git tracks any changes made to your project, allows for ease of collaboration and previous versions are available to recover. 
 This follows one of Etters core approaches to ensuring accurate documentation.

4. I updated my Markdown file, but the website has not changed, why?
  * If your changes do not appear after refreshing the page, you might have to rebuild the files.
  Run the following command to regenerate your site:
  ```console
    mkdocs build
  ```

## Credits
* **Static Site generator:** `MkDocs` (https://www.mkdocs.org/)
* **Feedback Contributors:** DK and Marias, who provided feedback on the static site hosting guide


