# Host Resume Using GitHub Pages

## Purpose

A tutorial of how to host a resume on GitHub Pages while introducing and and demonstrating the principles of Andrew Etter's book, *Modern Technical Writing*.

## Prerequisites
* Resume formatted in Markdown ([sample resume]([resume](https://github.com/GurmanToor/GurmanToor.github.io/blob/main/resume.md)))
* GitHub account (create one [here](https://github.com/join))
* Markdown editor (see [More Resources](#more-resources) for recommendations)
* Web browser
* Computer running Linux terminal
	* Windows 10: Use [this tutorial](https://allthings.how/how-to-use-linux-terminal-in-windows-10/#:~:text=To%20do%20this%2C%20start%20type,click%20the%20'OK'%20button.) to setup Linux terminal
	* MacOS: Use Terminal application

## Instructions

### ▶︎ Setting up GitHub Pages
*Connection to Ettier's Book:* We use GitHub Pages so we can incorporate version control. GitHub repositories use version control which allow for better performance, offline work and are superior for concurrent work on the same file. Additionally, according to Ettier, it is strongly valuable to store your code and documentation in the same repository (such as this one) so that documentation and code branches stay in sync and other developers are more likely to contribute if they don't have to clone a seperate repository. Also, a README.md file (like this one) should be in the root of the repository that provides a quick summary of the product, instructions how to build the product and how to contribute to the product.

In order to host a resume on GitHub Pages, we must first create a repository on GitHub that runs GitHub Pages. 

1. Login to [GitHub](https://github.com)
    
    *Connection to Ettier's Book:* Links are helpful to guide the user to where exactly they need to go and can help to reduce the amount of steps. Also, they avoid duplication and redundancy as technical documentation should be as comprehensive as possible. 
    
2. Navigate to [create a new repository](https://github.com/new)
    
3. Enter *username*.github.io where *username* is your username on GitHub under "**Repository name**"

    *Connection to Ettier's Book:* In technical documentation, bold is used for user interface elements. In this case, repository name is an element on the GitHub webpage. 

4. Open your Linux terminal   
5. Navigate to the folder in which you want to store your repository
6. Clone the repository by entering:
    ```
    git clone https://github.com/username/username.github.io
    ```
    into the terminal.
    
    *Connection to Ettier's Book:* Monospace should be used for terminal code.
    
🎉 Congratulations! Your GitHub Pages website is now live at https://username.github.io

Now, we proceed to installing Jekyll so that we may generate static site content on our GitHub Pages website.

### ▶︎ Installing Jekyll

The installation process for Jekyll is a little more complicated and involves more steps.

Please reference [this guide](https://jekyllrb.com/docs/installation/) for installing Jekyll.

### ▶︎ Create a GitHub Pages site with Jekyll

*Connection to Ettier's Book:* Jekyll is a static website generator. According to Ettier, static websites are fast, simple, portable and secure. They run on zero server-side application dependencies, no databases, and no installation so moving a static site is as easy as moving a directory. For our resume, Jekyll is a great choice for generating a static website on GitHub Pages as Jekyll is highly compatible with GitHub Pages and is used in the backend to run GitHub Pages. Additionally, Jekyll is the most popular static site generator, therefore there will be lots of docuemntation and troubleshooting resources for it.  


(Note: A lot of these steps are taken from the docs on GitHub, [here](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/creating-a-github-pages-site-with-jekyll))

Now that we have GitHub Pages and Jekyll all set up, we can proceed to generating a Jekyll static site in our GitHub Pages repository. 

1. Open your Linux terminal
2. Navigate to the folder in which you stored your GitHub Pages repository
3. Enter the ```jekyll new``` command into the terminal to create a new Jekyll website
4. Open the Gemfile that Jekyll created
5. Add "#" to the beginning of the line that starts with ```gem "jekyll"``` to comment out this line
6. Add the github-pages gem by editing the line starting with ```# gem "github-pages"```. Change this line to: ```gem "github-pages", "~> GITHUB-PAGES-VERSION", group: :jekyll_plugins```

   *Note:* Replace GITHUB-PAGES-VERSION with the latest supported version of the ```github-pages``` gem. You can find this version [here](https://pages.github.com/versions/). 
   
7. Save and close the Gemfile
8. From the terminal, run ```sudo bundle install```
9. (Optional) Make changes to the ```_config.yml``` file. In this file, you can change the title, description and email information inside the website. 
10. Add your work to Git: ```git add --all```
11. Commit the changes: ```git commit -m "Initial GitHub pages site with Jekyll"```
12. Push the changes to your repository: ```git push -u origin main```

Your Jekyll site is now available on username.github.io

Now, we must add the contents of our resume to the Jekyll site.

### ▶︎ Add resume content to Jekyll site

*Connection to Ettier's Book:* We use a lightweight markup language to create our resume called Markdown. Lightweight markup languages such as Markdown are very human readable and easy for anyone to contribute to. Additionally, there are many "flavours" of Markdown that each have their own pros and cons. For example, "vanilla" Markdown allows for broad compatibility, but you don't get features that other flavours such as Markdown Extra and MultiMark have such as tables and "fenced" code blocks. According to Ettier, Markdown is a very popular markup language that will continue to develop at a fast rate which makes it quite "future-proof" and is a great choice to use in your documentation and website content. 

Since, the main body of the Jekyll site is stored inside the ```index.md``` file, all we need to do is copy and paste the markdown code of our ```resume.md``` (from prerequisites) into the ```index.md``` file. 

1. Navigate to the folder in which our repository is stored
2. Open the ```index.md``` file
3. Copy contents of the ```resume.md``` file
4. Paste contents of ```resume.md``` at bottom of ```index.md``` file under the separation line below ```layout: home```

    **Warning:** Do not delete front matter content of file. Only add information below separation line of ```layout: home```
5. Save and close the ```index.md``` file
6. Add your work to Git: ```git add --all```
7. Commit your changes: ```git commit -m "Added resume content to index.md"```
8. Push the changes to your repository: ```git push -u origin main```

🤩 Yay, you're all done! Navigate to username.github.io on your web browser and view your resume on your static Jekyll site hosted by GitHub Pages. 

![](https://github.com/GurmanToor/GurmanToor.github.io/blob/main/resume.gif)


### More Resources
* [Markdown Tutorial](https://www.markdowntutorial.com/)
* [Linux Commands](https://www.guru99.com/linux-commands-cheat-sheet.html)
* [*Modern Technical Writing*](https://www.amazon.ca/Modern-Technical-Writing-Introduction-Documentation-ebook/dp/B01A2QL9SS) by Andrew Etter
* [Markdown Editors](https://www.oberlo.ca/blog/markdown-editors)

## Authors and Acknowledgements

* Built on the principles of Andrew Etter's book, *Modern Technical Writing* 
* Some steps taken from GitHub documentation for [Creating a GitHub Pages site with Jekyll](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/creating-a-github-pages-site-with-jekyll)
* Template for resume taken from [sdsawtelle/markdown-resume](https://github.com/sdsawtelle/markdown-resume)
* Thank you to these amazing people for peer reviewing this README:
	* Al Fahiyan Siyam
	* Felix Wedel
	* Nurida Karimbaeva
* Written by Gurman Toor

## FAQs

### Why is Markdown better than a word processor?

Markdown is better than a word processor for certain things. Word processors are great for creating short and attractive PDF's that have a single-use, for reading and discarding. However, when it comes to writing technical documentation, we need something that can be updated frequently for the long-term. Markdown is very compatible with version control systems and can be updated frequently with ease, rather than something such as Word's DOCX file format which is a hassle to deal with version control.

Additionally, documentation should be widely available online. Word's HTML export feature is highly unreliable and ineffective for building websites. In contrast, Markdown is very compatible when creating websites with minimal overhead. Also, Markdown is completely free to use while word processors (such as Microsoft Word) can cost money and are limited to certain operating systems. 

### How can I test my website locally?

If you want to test your site locally before committing the changes to your GitHub Pages repository, follow these steps:

1. Open your Linux terminal
2. Navigate to the folder in which your repository is located
3. Enter the command: ```bundle exec jekyll serve```
4. Open your web browser
5. Enter ```http://localhost:4000/``` into the search bar and hit enter

Your website is now hosted locally and you may review your changes as necessary. Enter ctrl+c in the terminal to stop the local server. 



