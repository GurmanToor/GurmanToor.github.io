# Host Resume Using GitHub Pages

## Purpose

A tutorial of how to host a resume on GitHub Pages while introducing and and demonstrating the principles of Andrew Etter's book, *Modern Technical Writing*.

## Prerequisites
* Resume formatted in Markdown ([sample resume]([resume](https://github.com/GurmanToor/GurmanToor.github.io/blob/main/resume.md)))
* GitHub account (create one [here](https://github.com/join))
* Computer running Linux terminal
	* Windows 10: Use [this tutorial](https://allthings.how/how-to-use-linux-terminal-in-windows-10/#:~:text=To%20do%20this%2C%20start%20type,click%20the%20'OK'%20button.) to setup Linux terminal
	* MacOS: Use Terminal application

## Instructions

### Setting up GitHub Pages
In order to host a resume on GitHub Pages, we must first create a repository on GitHub that runs GitHub Pages.

1. Log in to [GitHub](https://github.com)
2. Navigate to [create a new repository](https://github.com/new)
3. Under "**Repository name**", enter *username*.github.io where *username* is your username on GitHub.
4. Open your Linux terminal
5. In your terminal, navigate to the folder in which you want to store your repository
6. Clone the repository by entering:
    ```
    git clone https://github.com/username/username.github.io
    ```
    into the terminal.
    
Congratulations! Your GitHub Pages website is now live at https://username.github.io

Now, we proceed to installing Jekyll so that we may generate static site content on our GitHub Pages website.

### Installing Jekyll

The installation process for Jekyll is a little more complicated and involves more steps.

Please reference [this guide](https://jekyllrb.com/docs/installation/) for installing Jekyll.

### Create a GitHub Pages site with Jekyll

(Note: A lot of these steps are taken from the docs on GitHub, [here](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/creating-a-github-pages-site-with-jekyll))

Now that we have GitHub Pages and Jekyll all set up, we can proceed to generating a Jekyll site in our GitHub Pages repository. 

1. Open your Linux terminal
2. Navigate to the folder in which you stored your GitHub Pages repository
3. To create a new Jekyll site, enter the ```jekyll new``` command into the terminal
4. Open the Gemfile that Jekyll created
5. Add "#" to the beginning of the line that starts with ```gem "jekyll"``` to comment out this line
6. Add the github-pages gem by editing the line starting with ```# gem "github-pages"```. Change this line to: ```gem "github-pages", "~> GITHUB-PAGES-VERSION", group: :jekyll_plugins```

   Replace GITHUB-PAGES-VERSION with the latest supported version of the ```github-pages``` gem. You can find this version [here](https://pages.github.com/versions/). 
   
7. Save and close the Gemfile
8. From the terminal, run ```sudo bundle install```
9. (Optional) Make changes to the ```_config.yml``` file. In this file, you can change the title, description and email information inside the website. 
10. Add your work to Git: ```git add --all```
11. Commit the changes: ```git commit -m "Initial GitHub pages site with Jekyll"```
12. Push the changes to your repository: ```git push -u origin main```

Your Jekyll site is now available on username.github.io

Now, we must add the contents of our resume to the Jekyll site.

### Add resume content to Jekyll site

Since, the main body of the Jekyll site is stored inside the ```index.md``` file, all we need to do is copy and paste the markdown code of our ```resume.md``` (from prerequisites) into the ```index.md``` file. 

1. Navigate to the folder in which our repository is stored
2. Open the ```index.md``` file
3. Copy contents of the ```resume.md``` file
4. Paste contents of ```resume.md``` at bottom of ```index.md``` file under the separation line below ```layout: home```
5. Save and close the ```index.md``` file
6. Add your work to Git: ```git add --all```
7. Commit your changes: ```git commit -m "Added resume content to index.md"```
8. Push the changes to your repository: ```git push -u origin main```

Congratulations, you're all done! Navigate to username.github.io and view your resume on your static Jekyll site hosted by GitHub Pages. 


### More Resources
* [Markdown Tutorial](https://www.markdowntutorial.com/)
* [Linux commands](https://www.guru99.com/linux-commands-cheat-sheet.html)
* [*Modern Technical Writing*](https://www.amazon.ca/Modern-Technical-Writing-Introduction-Documentation-ebook/dp/B01A2QL9SS) by Andrew Etter

## Authors and Acknowledgements

* Built on the principles of Andrew Etter's book, *Modern Technical Writing* 
* Some steps taken from GitHub documentation for [Creating a GitHub Pages site with Jekyll](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/creating-a-github-pages-site-with-jekyll)
* Template for resume taken from [sdsawtelle/markdown-resume](https://github.com/sdsawtelle/markdown-resume)

## FAQs

### Why is Markdown better than a word processor?

Word processors are great for creating short and attractive PDF's that have a single-use, for reading and discarding. However, when it comes to writing technical documentation, we need something that can be updated frequently, long-term. Markdown is very compatible with version control systems and can be updated frequently with ease, rather than something such as Word's DOCX file format which is a hassle to deal with version control.

Additionally, documentation should be widely available online. Word's HTML export feature is highly unreliable and ineffective for building websites. In contrast, Markdown is very compatible when creating websites with minimal overhead. Also, Markdown is completely free to use while word processors (such as Microsoft Word) can cost money and are limited to certain operating systems. 

### 

