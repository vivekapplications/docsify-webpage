# Project1: Docsify



### Introduction

> Docsify is an open-source tool which helps in generating webpages for documention of a project - be it software related or not.

> Document of a project creates a central access point for information and a way to know what was done & when, making it easier to track changes.

> Generally software developers' focus is on writing code and most of their time is spent in the same. They don't have enough time for creating a webpage for the documentation of their software product or service. Docsify can make their task of generating document easy and less time consuming.

> It does not generate static html files for creating webpages. It smartly loads Markdown files, analyses them syntactically using Marked as a parser and displays them as a webpage. 



### Key features & benefits

- It does not creates static html files.

- It keeps the website simple & lighweight.

- It enables smart full-text search plugin.

- It provides multiple themes.

- It provides useful plugin API.

- It also supports emoji.

   

Here is an example of website which was generated using docsify. 

https://security-list.js.org/#/



### Requirments for installation & setup

> To know the exact system requirements for docsify installation run the below mentioned command on the terminal of the system.

> Command: cat /etc/os-release

PRETTY_NAME="Ubuntu 22.04.3 LTS"
NAME="Ubuntu"
VERSION_ID="22.04"
VERSION="22.04.3 LTS (Jammy Jellyfish)"
VERSION_CODENAME=jammy
ID=ubuntu
ID_LIKE=debian
HOME_URL="https://www.ubuntu.com/"
SUPPORT_URL="https://help.ubuntu.com/"
BUG_REPORT_URL="https://bugs.launchpad.net/ubuntu/"
PRIVACY_POLICY_URL="https://www.ubuntu.com/legal/terms-and-policies/privacy-policy"
UBUNTU_CODENAME=jammy



### Required software & tools

Node.js & NPM (Node Package Manager)

> JavaScript has a vast library. These libraries are used in various types of projects.
> Those JS libraries which are intended to be used in a node.js project are widely being managed by Node Package Manager (NPM).

> Node.js provides a JavaScript-based platform which is used to develop web applications. Docsify is one of those JS libraries which are used in a node.js project to develop web applications & it uses NPM as a package manager.

### Node.js

1. Node.js helps the docsify in making content available on the server side.
   In case the website is hosted on a remote server and being searched( by a user ) using Google search engine via website's domain name, provided the website is built using docsify, the node.js helps in making the content of the website available on the Google web server side smoothly.
2. Node.js also helps the docsify in running local development server. This local server allows the user to preview and develop the document locally on his computer before deploying it to the production environment.
3. Node.js ensures the cross-platform compatibility of the projects developed using docsify. This means that the website developed using docsify on one platform ( operating system ) can be easily shared and run on different platforms.
4. Node.js supports the use of plugins in the docsify.
5. Docsify take the help of node.js during the build and compilation process.
   Major points included in the build & compilation process are mentioned below.
   a. Conversion of Markdown files into HTML to deliver the content as a webpage.
   b. Navigation & Sidebar generation for structuring the documentation layout.
   c. Achor tags & header links to facilitate easy navigation within the document.
   d. Injection of scripts for dynamic behaviour of the website such as live reloading, search functionality & smooth scrolling.
   To inject scripts user has to mention the script within the script tags in the HTML file.
   Once the script gets mentioned the docsify makes the website interactive and dynamic.
   e. Local server setup to preview the webpage during the development phase.
   f. After completion of the build process, the compiled content is ready for deployment on the web servers or hosting platform.

### Node Package Manager

1. Docsify is one of the libraries of JS. It may have dependencies on other JS libraries or tools. NPM helps the docsify user to install and manage those required dependencies. So it helps in dependency management.
2. NPM allows the user to specify the version of docsify and its dependencies on a file named 'package.json'. This file is available in the project made by the user. NPM ensures that everyone working on the same project uses the same version, reducing compatibility issues.
3. NPM helps in script execution which is used to automate various tasks related to the project, such as starting the local development server, building the documentation & deploying the website.
4. NPM also helps in initializing a new project made using docsify.



### Step by step guide to installation & setup

> The user needs to follow the below mentioned steps to install & setup docsify to use it to generate the webpages. 

**Step1**

- Command: sudo apt update

Description: This command will update the system of the user.

**Step2**

- Command: sudo apt install nodejs

Description: This command will install nodejs on the system of the user

**Step3**

- Command: sudo apt install npm

Description: This command will install npm on the system of the user.

**Step4**

Now the user needs to make a new directory. He can name the directory according to his own choice.

- Command: mkdir Projects

Now the user needs to change his working location on the terminal to enter into the newly made directory (Projects).

- Command: cd Projects

**Step5**

- Command: npm init -y

This command will create a package.json file into the newly made directory. It is the configuration file for JS packages which are being managed by the NPM. Here y denotes yes.

**Step6**

- Command: sudo npm install -g docsify-cli

This command will allow the user to install docsify-cli with the help of npm globally on the entire system of the user.
Now since the docsify-cli is globally installed, the user can create his website with the below mentioned steps.

**Step7** 

- Command: docsify init Project1

This command will create and initialize a new directrory with name Project1 inside the current directory Projects. As soon as the directory Project1 is created, two other files will also get created inside it named index.html & README.md.
The first one is the html file for the Project1(a webpage) created using docsify and the second one is the Markdown file in which user writes the content to be diplayed on the webpage.

Once the user has entered this command. There will be a message saying ' Initialization Succeeded! '  Please run docsify serve Project1 

**Step8**

- Command:  docsify serve Project1

This command will start a local server and the user can access his docsify documentation in his web browser by visiting the url mentioned i.e. http://localhost:3000 

To stop serving use ctrl + z
There will be a message indicating 'Stopped   docsify serve Project1'

To restart serving use command: fg 
(fg stands for foreground)
There will be a message indicating 'docsify serve Project1'

#### Note

If the user has stopped the local server and closed the terminal and want to edit the content of the Markdown file and run it again on the web browser then he does not need to initialize the Project1 again.
Without initializing he can directly go to the Project1 directory and run the command: 

docsify serve .

There is a space between serve & (.)
Here (.) means current working directory.
Once the user runs this command, the content of the Markdown file in the current working directory (Project1) will start getting displayed on the web browser.



### Configuration options in docsify

> Docsify provides a range of configurations options so that the user can customize the behavior and appearance of his webpage.
> Some of these configuration options are explain below:

**Main Configuration**

a.  el: In docsify el is 'element selector'. It refers to a CSS selector that identifies the HTML element where docsify will mount and render the documentation content. 
In the example shown below, el is the property used to define the element selector and #app is the ID, termed as the element selector.
The user can cumtomise the element selector according to the HTML structure of his documentation.

b. repo: It provides the GitHub repository information.

c. maxLevel: It indicates the maximum heading level for the sidebar.

d. loadSidebar: User can set it to 'false' if he wants to disable the sidebar.

Example:

window.$docsify = {
  el: '#app',
  repo: 'username/repo',
  maxLevel: 3,
  loadSidebar: true
};



**Markdown Configuration**

a. basePath: It is mentioned to resolve the relative links in Markdown files.

b. markdown: Additional Markdown-it plugins.

c. coverpage: Configuration for the cover page.

Example: 

window.$docsify = {
  basePath: '/docs/',
  markdown: {
    lineNumbers: true
  },
  coverpage: true
};



**Theme Configuration**

a. themeColor: Theme color for mobile browsers.

b. name: Name of the theme.

c. themeable: Allows custom styling via CSS variables.

Example:

window.$docsify = {
  themeColor: '#3F51B5',
  name: 'custom-theme',
  themeable: {
    ready: customThemeReady
  }
};



**Navigation Configuration**

a. alias: Redirects or alternate path name for specific pages.

b. auto2top: Scrolls to the top on page change.

Example:

window.$docsify = {
  alias: {
    '/docs/zh-cn/guide': '/docs/guide',
    '/zh-cn/api': '/api'
  },
  auto2top: true
};



**Search Configuration**

a. search: Configuration for the search feature.

Example:

window.$docsify = {
  search: {
    maxAge: 86400000, // 1 day
    paths: 'auto',
    placeholder: 'Search'
  }
};



> Apart from these options there are many more options available in Docsify.



### Plugins & Extensions

> Docsify supports a variety of plugins & extensions to enhance its functionality. These plugins & extensions allow the user to customize the features of his documentation site.
>
> To use a plugin the user has to include its script in the 'index.html' file.

> Some common plugins & extensions available with docsify are mentioned below:

1. Search Plugin: It adds the search functionality to the documentation site and allows the user to search for a specific content.

   Example: docsify-plugin-search

2. Emoji Plugin: It allows the user to use emojis in the document.

   Example: docsify-plugin-emoji

3. Zoom Image Plugin: It provides zoom in option by clicking on images.

   Example: docsify-plugin-zoom-image

4. Copy to Clipboard Plugin: It adds a 'Copy to Clipboard' button to code blocks to make it easy for the user to copy code snippets.

   Example: docsify-copy-code

5. External Link Target Plugin: It opens external link in a new tab.

   Example: docsify-plugin-external-link-target

6. Reading Time Plugin: It adds an estimated reading time to each page.

   Example: docsify-reading-time

7. Tabs Plugin: It creat tabs to organize & display content.

   Example: docsify-tabs

8. Embed Files Plugin: It allows embeding files (e.g. PDF, images) directly into the documentation.

   Example: docsify-embed-files



### Integration & Deployment of Docsify with GitHub

A user can easily integrate Docsify with GitHub by using GitHub Pages.
GitHub Pages is designed to host project pages from GitHub repository.

1. Login into GitHub profile.
2. Go to the repository of the project.
3. Go to the setings.
4. On the settings page, confirm that the 'default branch' should be 'main' or 'master'.
5. Under general settings go to 'code and automation' & click 'Pages.'
6. Choose 'Deploy from a branch' as a source under 'Build & Deployment'.
7. Now select 'main' branch & 'root' folder and click 'save'.
8. Now again go to the repository of the project & upload the file (markdown) using 'add file' and click on 'commit changes'. 
9. Again go to the settings under repository and click pages then click on 'visit site'.
10. Now the website made using docsify is visible.
